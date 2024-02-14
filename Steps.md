Send data from delivery boy see the location in End User
  2 Spring Boot Project Run Delivery Boy And See the output Via End User Send Message from Postman and See the output on consumer group location-test-update topic created and See the location 
Run zookeeper 
		zookeeper-server-start.bat ..\..\config\zookeeper.properties
Run kafka Services at the back
		kafka-server-start.bat ..\..\config\server.properties
Create topic
		kafka-topics.bat --create --topic location-test-update --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3

Run Delivery boy and End User in Spring Boot 
Open Postman Hit the Url
See the message 
![image](https://github.com/Lehar1107/SendDataFRomOneToAnother/assets/126607616/db698517-727b-4e14-becc-82a8a4af4b62)



Run the Consumer Comand 
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic location-test-update --from-beginning
	

![image](https://github.com/Lehar1107/SendDataFRomOneToAnother/assets/126607616/539f0fea-ecff-4a03-b0b4-e27543c1ff54)
