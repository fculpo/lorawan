FROM ubuntu:16.04
MAINTAINER Fabien Culpo <fabien.culpo@gmail.com>

RUN apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

RUN useradd -ms /bin/bash lorauser
USER lorauser
WORKDIR /home/lorauser

RUN wget https://github.com/brocaar/lora-app-server/releases/download/0.7.2/lora_app_server_0.7.2_linux_amd64.tar.gz -O lora-app-server.tar.gz \
 && tar xvf lora-app-server.tar.gz

CMD ./lora-app-server

EXPOSE 8080
