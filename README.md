# kafka-zookeeper

## Run Zookeeper Service (keep window open)
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

## Run Kafka Service (keep window open)
.\bin\windows\kafka-server-start.bat .\config\server.properties

## Create List, Topic, or Delete Topics (temporary window)
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic jacks information 
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list

## Run Kafka Producer to Add Material into List (keep window open)
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic jacks information
> Item 1
> Item 2
> Item 3

## Run Kafka Consumer that Reorders and Shows List Contents (keep window open)
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic jacks information --from-beginning
