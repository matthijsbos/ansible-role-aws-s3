FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    software-properties-common
RUN add-apt-repository universe
RUN apt-get update && apt-get install -y \
    python \
    python-pip
RUN pip install awscli
