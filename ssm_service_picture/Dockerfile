FROM openjdk:8-jre-alpine

MAINTAINER lzh <liao08022040@126.com>

ARG JAR_FILE
ENV JAR_FILE ${JAR_FILE}

COPY target/${JAR_FILE} /tmp
COPY target/lib/ /tmp/lib/

WORKDIR /tmp

EXPOSE 20880

CMD java -jar ${JAR_FILE}

