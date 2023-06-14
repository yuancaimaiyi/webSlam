FROM nvidia/cuda:10.2-devel-ubuntu18.04
MAINTAINER cheng.li
ARG DEBIAN_FRONTEND=noninteractive
# Prepare and empty machine for building
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A4B469963BF863CC
RUN cp /etc/apt/sources.list /etc/apt/sources.list.bak
#RUN sed -i s:/archive.ubuntu.com:/mirrors.aliyun.com/ubuntu:g /etc/apt/sources.list
RUN sed -i s:/archive.ubuntu.com:/mirrors.tuna.tsinghua.edu.cn/ubuntu:g /etc/apt/sources.list
RUN apt-get update && apt-get install -y \
    git \
    cmake \
    vim \
    build-essential \
    libboost-program-options-dev \
    libboost-filesystem-dev \
    libboost-graph-dev \
    libboost-system-dev \
    libboost-test-dev \
    libeigen3-dev \
    libsuitesparse-dev \
    libfreeimage-dev \
    libgoogle-glog-dev \
    libgflags-dev \
    libglew-dev \
    qtbase5-dev \
    libqt5opengl5-dev \
    libcgal-dev \
    libcgal-qt5-dev \
    libjsoncpp-dev  \
    libxml2-dev  \
    wget \
    curl 

COPY install.sh .
RUN chmod a+x ./install.sh && ./install.sh 
RUN /bin/bash 
RUN /bin/bash -c "source ~/.bashrc"
#RUN nvm ls-remote  
RUN apt-get -y install python3-pip 
RUN pip3 install requests
#RUN nvm install v14.17.6
