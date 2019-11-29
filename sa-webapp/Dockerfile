#FROM maven:3.5-jdk-8-alpine AS builder
FROM maven:3.6.2-jdk-13 AS builder
COPY src /sa-webapp/src
COPY pom.xml /sa-webapp
RUN mvn -f /sa-webapp/pom.xml clean package

ENV SA_LOGIC_API_URL http://localhost:5000

#FROM openjdk:8-jre-alpine
FROM openjdk:13.0.1-jdk-buster
COPY --from=builder /sa-webapp/target/sentiment-analysis-web-0.0.1-SNAPSHOT.jar ./
EXPOSE 8080
CMD ["java", "-jar", "sentiment-analysis-web-0.0.1-SNAPSHOT.jar", "--sa.logic.api.url=${SA_LOGIC_API_URL}"]