FROM maven as build
MAINTAINER sarat.e99@gmail.com Sarat Chandra E


WORKDIR /app
COPY . .
RUN mvn install

#jdk
FROM openjdk:8-jdk-alpine #openjdk:11.0.10-jre
MAINTAINER sharan
WORKDIR /app
COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app 

EXPOSE 9999

CMD ["java", "-jar", "zuul-0.0.1-SNAPSHOT.jar"] 
