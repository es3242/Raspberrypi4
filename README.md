# Raspberrypi4

//docker file 생성후 이미지 build 
$ sudo docker build --tag <image name>:<tag>

//docker login
$ docker login

//이미지 push
$ docker push <DOCKER_HUB_ID>/<image name>:<tag>

-------APM 환경 구성 DOCKERFILE 만들기-------

# ubuntu 이미지 16.04로부터 새로운 이미지를 만듭니다. 
# ":16.04"를 생략하면 latesd 버전을 기본 이미지로 합니다.
FROM ubuntu:16.04
# MAINTAINER는 이미지를 생성한 사람의 정보를 설정. 
# 형식은 자유, 일반적으로 이름과 이메일로 합니다.
MAINTAINER EUNSIL CHO <eunsil3242@naver.com>
# src 디렉토리 생성 및 디렉토리 이동
RUN mkdir src
WORKDIR /src

# 우분투 패키지 갱신
RUN apt-get update

# apache2 설치
RUN apt-get install -y apache2

# php 설치
RUN apt-get install 
# Bitcoin Core 소스 코드 및 라이브러리 다운로드
RUN git clone https://github.com/bitcoin/bitcoin.git

# 컴파일러 gcc 설치
RUN apt-get install -y build-essential automake pkg-config libevent-dev bsdmainutils

# OpenSSL 설치
RUN apt-get install -y libtool autotools-dev autoconf libssl-dev


# 관련 라이브러리 설치
RUN apt-get install -y libminiupnpc-dev libqrencode-dev

# GUI 라이브러리 설치
RUN apt-get install -y libqt5gui5 libqt5core5a libqt5dbus5 
RUN apt-get install -y qttools5-dev qttools5-dev-tools
RUN apt-get install -y libprotobuf-dev protobuf-compiler



출처: https://mystarlight.tistory.com/171 [커피향처럼]
