FROM ubuntu:16.04
MAINTAINER Fabien Culpo <fabien.culpo@gmail.com>

RUN apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

RUN useradd -ms /bin/bash lorauser
USER lorauser
WORKDIR /home/lorauser

RUN wget https://github.com/brocaar/loraserver/releases/download/0.16.1/loraserver_0.16.1_linux_amd64.tar.gz -O loraserver.tar.gz \
 && tar xvf loraserver.tar.gz

CMD ./loraserver

