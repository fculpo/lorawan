FROM ubuntu:16.04
MAINTAINER Fabien Culpo <fabien.culpo@gmail.com>

RUN apt-get update \
  && apt-get install -y wget \
  && rm -rf /var/lib/apt/lists/*

RUN useradd -ms /bin/bash lorauser
USER lorauser
WORKDIR /home/lorauser

RUN wget https://github.com/brocaar/lora-gateway-bridge/releases/download/2.1.4/lora_gateway_bridge_2.1.4_linux_amd64.tar.gz \
      -O lora-gateway-bridge.tar.gz \
 && tar xvf lora-gateway-bridge.tar.gz

CMD ./lora-gateway-bridge

EXPOSE 1700/udp
