FROM tomcat:9.0-jdk8-corretto-al2

LABEL maintainer="phithon <root@leavesongs.com>"

RUN sed -i 's/securerandom.source=file:\/dev\/urandom/securerandom.source=file:\/dev\/.\/urandom/g' $JAVA_HOME/lib/security/java.security
