FROM python:3.12.1-slim

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get -y install --reinstall ca-certificates && \
    apt-get -y install openjdk-17-jdk wget unzip

RUN pip install --upgrade pip && \
    pip install ipykernel jupyter

RUN mkdir -p ijava && \
    cd ijava && \
    wget https://github.com/SpencerPark/IJava/releases/download/v1.3.0/ijava-1.3.0.zip && \
    unzip ijava-1.3.0.zip && \
    python3 install.py --sys-prefix && \
    cd .. && \
    rm -rf ijava