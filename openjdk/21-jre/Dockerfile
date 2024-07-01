FROM ubuntu:24.04

ARG container_user=mosip
ARG container_user_group=mosip
ARG container_user_uid=1001
ARG container_user_gid=1001

ENV container_user=${container_user}
ENV container_user_group=${container_user_group}
ENV container_user_uid=${container_user_uid}
ENV container_user_gid=${container_user_gid}

ENV JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64
ENV PATH=/usr/lib/jvm/java-21-openjdk-amd64/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
ENV JAVA_VERSION=21
ENV LANG=C.UTF-8

# Install mc and its dependencies
RUN apt-get update && \
    apt-get install -y --no-install-recommends openjdk-21-jre wget unzip && \
    java --version
