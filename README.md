# kafka-learning
Kafka CLI:
- Create Topic:
kafka-topics --zookeeper 127.0.0.1:2181 --topic first_topic --create --partitions 3 --replication-factor 2
- Listing all topics:
kafka-topics --zookeeper 127.0.0.1:2181 --list
- Describe topic:
kafka-topics --zookeeper 127.0.0.1:2181 --topic first_topic --describe
- Send message to a topic:
kafka-console-producer --broker-list 127.0.0.1:9092 --topic first_topic
- Read messages from a topic:
kafka-console-consumer --bootstrap -server 127.0.0.1:9092 --topic first_topic
  This will read current messages only
- Read all messages:
kafka-console-consumer --bootstrap-server 127.0.0.1:9092 --topic first_topic --from-beginning
- Consumer Group:
kafka-console-consumer --bootstrap-server 127.0.0.1:9092 --topic first_topic --group my-application-group
- Reset consumer group offsets:
kafka-consumer-groups --bootstrap-server localhost:9092 --group my-application-group --reset-offsets --to-earliest --execute --topic first_topic
