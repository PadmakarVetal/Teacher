FROM maven:3.9.9-eclipse-temurin-17 AS build
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn -DekipTests package

FROM eclipse-temurin:1
WORKDIR /app7-jre
COPY --from=build /app/targer/*.jar app.jar
ENTRYPOINT ["java","-jar","app.jar"]