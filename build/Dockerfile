FROM openjdk:8-jre-alpine3.9
MAINTAINER leo18945 "leo18945@gmail.com"

# set environment
ENV MODE="cluster" \
    PREFER_HOST_MODE="ip"\
    BASE_DIR="/home/nacos" \
    CLASSPATH=".:/home/nacos/conf:$CLASSPATH" \
    CLUSTER_CONF="/home/nacos/conf/cluster.conf" \
    FUNCTION_MODE="all" \
    JAVA_HOME="/usr/lib/jvm/java-1.8-openjdk/jre" \
    NACOS_USER="nacos" \
    JAVA="/usr/lib/jvm/java-1.8-openjdk/jre/bin/java" \
    JVM_XMS="2g" \
    JVM_XMX="2g" \
    JVM_XMN="1g" \
    JVM_MS="128m" \
    JVM_MMS="320m" \
    NACOS_DEBUG="n" \
    TOMCAT_ACCESSLOG_ENABLED="false" \
    TZ="Asia/Shanghai"

ARG NACOS_VERSION=1.3.0

RUN addgroup -S nacos \
    && adduser -S nacos -G nacos \
    && apk add --no-cache tini

USER nacos
WORKDIR /$BASE_DIR

ADD . .

RUN mkdir -p logs \
	&& cd logs \
	&& touch start.out \
	&& ln -sf /dev/stdout start.out \
	&& ln -sf /dev/stderr start.out

EXPOSE 8848
ENTRYPOINT ["/sbin/tini", "--", "bin/docker-startup.sh"]