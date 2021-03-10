FROM blauerberg/drupal-php:7.4-fpm
MAINTAINER Yoshikazu Aoyama <yskz.aoyama@gmail.com>

ENV TIKA_VERSION 1.13

RUN mkdir -p /usr/share/man/man1
RUN apt-get update -y \
    && apt-get install -y openjdk-11-jre-headless \
    && apt-get autoclean \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /var/cache/apt/archives/*

RUN mkdir -p /var/lib/tika \
    && cd /var/lib/tika \
    && curl -O http://archive.apache.org/dist/tika/tika-app-${TIKA_VERSION}.jar
