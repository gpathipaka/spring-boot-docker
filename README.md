#Build Project
mvn clean install

#Runt the project
java -jar target/spring-boot-docker-0.0.1-SNAPSHOT.jar    

#Build Docker Image form Dockerfile
docker build -t gp/spring-boot-app .

#RUN the Docker Image
docker run -p 8080:8080 gp/spring-boot-app

#Actuator end point
http://localhost:8080/actuator


