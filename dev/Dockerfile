
FROM debian:latest

RUN set -e &&\
    sed -i 's/deb\.debian\.org/mirrors.aliyun.com/' /etc/apt/sources.list &&\
    sed -i 's/deb-src/# deb-src/' /etc/apt/sources.list &&\
    apt-get update

RUN apt-get install -y --no-install-recommends\
        build-essential\
        vim-tiny\
        python\
        curl\
        git\
        wget\
        locales

RUN rm -rf \
    /var/lib/apt/lists/* \
    /tmp/* \
    /var/tmp/* \

RUN mkdir /source
