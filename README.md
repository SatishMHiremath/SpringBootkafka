# SpringBootkafka
Spring Boot Kafka Message Stream

Download Kafka distribution from the below url:
https://kafka.apache.org/downloads

#Start Apache Zookeeper-
C:\kafka_2.12-0.10.2.1>.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

#Start Apache Kafka-
C:\kafka_2.12-0.10.2.1>.\bin\windows\kafka-server-start.bat .\config\server.properties

#Next start the Spring Boot Application by running it as a Java Application.
#Also Start the consumer listening to the upstream_in_use_topic-
C:\kafka_2.12-0.10.2.1>.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic upstream_in_use_topic --from-beginning

Finally hit the url as follows- http://localhost:8080//javainuse-kafka/producer?message=test

This will trigger the message to be sent to the upstream_in_use_topic. We can see in the consumer started the message is recieved
C:\kafka_2.12-0.10.2.1>.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic upstream_in_use_topic --from-beginning
