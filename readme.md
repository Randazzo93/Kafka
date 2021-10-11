# Kafka commands need kafka booted up on server first (older version of kakfa need zookeeper booted up as well)
> zookeeper-server-start.bat config\zookeeper.properties
> 
> kafka-server-start.bat config\server.properties

# Topic Commands
### Create Topic (Replication factor should be 2 or more to assure data is not lost when a broker goes down)
> kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 3 --partitions 3 --topic test

### List Topics
> kafka-topics.bat --list --zookeeper localhost:2181

### Describe Topics
> kafka-topics.bat --describe --zookeeper localhost:2181 --topic test



# Producer Commands
> kafka-console-producer.bat --broker-list localhost:9092 --topic test


# Consumer Commands
> kafka-console-consumer.bat --zookeeper localhost:2181 --topic test
