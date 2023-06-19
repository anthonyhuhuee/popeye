FROM maven:3.8.4-jdk-11-slim AS builder

CMD ["mvn", "dependency:resolve"]
CMD ["mvn", "package"]

WORKDIR /worker-jar-with-dependencies.jar

FROM openjdk:11-jre-slim

CMD ["java", "-jar worker-jar-with-dependencies.jar"]