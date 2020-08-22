from ubuntu:18.04

RUN apt-get update && apt-get upgrade -y

COPY files/nointeractive.sh /tmp/
RUN chmod +x /tmp/nointeractive.sh && /tmp/nointeractive.sh

RUN apt install -y git make python3 python3-pip python3-sphinx python3-sphinx-rtd-theme latexmk texlive-xetex
