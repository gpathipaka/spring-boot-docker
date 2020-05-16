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


docker images 

aws ecr create-repository --name test

aws ecr describe-repositories 

$(aws ecr get-login --registry-ids [repo_id] --no-include-email)

docker tag Image_id:1.0.0 [repo_id].dkr.ecr.us-east-1.amazonaws.com/gp:app-0.0.1

docker push [repo_id].dkr.ecr.us-east-1.amazonaws.com/gp:app-0.0.1


