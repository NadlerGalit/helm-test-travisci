# This Dockerfile is to build the needed nsenter for Ubuntu 14.04, which is needed for helm
FROM ubuntu:14.04

RUN apt-get update && \
    apt-get install -y git bison build-essential libncurses5-dev libslang2-dev gettext zlib1g-dev libselinux1-dev debhelper lsb-release pkg-config po-debconf autoconf automake autopoint libtool && \
    git clone git://git.kernel.org/pub/scm/utils/util-linux/util-linux.git util-linux && \
    cd util-linux/ && \
    ./autogen.sh && \
    ./configure --without-python --disable-all-programs --enable-nsenter && \
    make


