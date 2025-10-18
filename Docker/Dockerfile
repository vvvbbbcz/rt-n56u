ARG http_proxy
ARG https_proxy
ARG all_proxy

FROM docker.m.daocloud.io/library/ubuntu:20.04

ENV http_proxy=${http_proxy}
ENV https_proxy=${https_proxy}
ENV all_proxy=${all_proxy}
ENV DEBIAN_FRONTEND=noninteractive

ADD ./sources.list /etc/apt/sources.list

WORKDIR /opt/rt-n56u

RUN apt-get update && \
    apt-get install -y \
    unzip \
    libtool-bin \
    curl \
    cmake \
    gperf \
    gawk \
    flex \
    bison \
    nano \
    xxd \
    fakeroot \
    kmod \
    cpio \
    git \
    python3-docutils \
    gettext \
    automake \
    autopoint \
    texinfo \
    build-essential \
    help2man \
    pkg-config \
    zlib1g-dev \
    libgmp3-dev \
    libmpc-dev \
    libmpfr-dev \
    libncurses5-dev \
    libltdl-dev \
    wget \
    libc-dev-bin \
    # 清理缓存以减小镜像体积
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]

