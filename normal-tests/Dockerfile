from ubuntu:22.04

RUN apt-get update && apt-get upgrade -y

COPY files/nointeractive.sh /tmp/
RUN chmod +x /tmp/nointeractive.sh && /tmp/nointeractive.sh

RUN apt-get install -y gcc g++ make qt5-qmake bison flex xxd git ssh docker
