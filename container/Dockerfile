FROM golang:1.21

RUN apt-get -y update && apt-get install -y --no-install-recommends \
    sudo \
    curl \
    git \
    wget \
    tzdata \
    && ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    && echo "Asia/Tokyo" > /etc/timezone \
    && dpkg-reconfigure -f noninteractive tzdata \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /opt/program
COPY app /opt/program/app
