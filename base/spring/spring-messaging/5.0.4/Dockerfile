FROM maven:3-jdk-8-alpine AS builder

COPY . /usr/src

RUN cd /usr/src; \
    mvn package

FROM openjdk:21-ea-13-jdk-oraclelinux8

LABEL maintainer="root <root@leavesongs.com>"

COPY --from=builder /usr/src/target/websocket-0.0.1-SNAPSHOT.jar /websocket-0.0.1-SNAPSHOT.jar

CMD ["java", "-jar", "/websocket-0.0.1-SNAPSHOT.jar"]
