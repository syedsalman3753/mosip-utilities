FROM ubuntu:20.04

ARG container_user=mosip
ARG container_user_group=mosip
ARG container_user_uid=1001
ARG container_user_gid=1001

ENV container_user=${container_user}
ENV container_user_group=${container_user_group}
ENV container_user_uid=${container_user_uid}
ENV container_user_gid=${container_user_gid}

# Install mc and its dependencies
RUN apt-get update && \
    apt-get install -y --no-install-recommends openjdk-17-jre wget && \
    java --version && \
    groupadd -g ${container_user_gid} ${container_user_group} && \
    useradd -u ${container_user_uid} -g ${container_user_group} -s /bin/bash -m ${container_user} && \
    mkdir -p /home/${container_user} \

