FROM ubuntu:latest

ENV TZ=Asia/Seoul LANG=ko_KR.UTF-8 LANGUAGE=ko_KR.UTF-8

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    locales tzdata build-essential sudo gdb vim curl git wget \
    python3 cmake make gcc sudo valgrind telnet net-tools iproute2\
    && locale-gen ko_KR.UTF-8 && update-locale LANG=ko_KR.UTF-8

RUN useradd -m -s /bin/bash jungle && usermod -aG sudo jungle

# 암호 설정 (빌드 시 ARG로 전달, 기본값은 환경변수에서)
ARG USER_PASSWORD=jungle
RUN echo "jungle:${USER_PASSWORD}" | chpasswd

USER jungle
WORKDIR /home/jungle