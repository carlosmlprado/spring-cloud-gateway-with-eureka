Simple project to represent the load balance with spring-cloud-gateway with simple configuration.

1 - Execute first eureka application

2 - Execute gateway application

3 - execute 2 instances of dummy app:

java -jar -Dserver.port=8055 target/dummy-0.0.1-SNAPSHOT.jar

java -jar -Dserver.port=8056 target/dummy-0.0.1-SNAPSHOT.jar

Send tests with Postman/Browser and check logs on Git or any Version Control you are using:

http://localhost:8074/dummy

Tests will reach the Gateway then will send requests to dummy application in both ports.
In logs We will can chack:
Getting dummy list from port: 8055
Getting dummy list from port: 8056
