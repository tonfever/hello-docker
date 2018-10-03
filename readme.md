# Sample Spring Boot WebApp
Run a spring boot webapp that simply returns a "Hello" style message when calling by GET method e.g. localhost:8080/{param}

## Docker commands to build, run and clean up

## Build image from a jar
docker build . -t demo/helloworld --build-arg JAR_FILE=target/helloworld-0.0.1-SNAPSHOT.jar

## Run container in deamon mode with name and port
docker run -p 8080:8080 -d --name=myhelloworld demo/helloworld

docker run -d -p 8080:8080 -v hellovol:/logback  --name=myhelloworld demo/helloworld

## Stop a running container
docker stop myhelloworld

## Remove the container
docker rm myhelloworld

## Remove the image
docker image rm demp/helloworld