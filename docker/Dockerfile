###########################################
# run using: 
# docker build -t ffbo/skeleton .
# docker run --name skeleton_component -v $(dirname `pwd`):/skeleton_component -it ffbo/neuroarch sh /skeleton_component/skeleton_component/run_component.sh
###########################################
FROM python:2

# File Author / Maintainer
MAINTAINER Adam Tomkins <a.tomkins@sheffield.ac.uk>
RUN apt-get update && apt-get install -y apt-transport-https

ENV HOME /app
ENV DEBIAN_FRONTEND noninteractive
ENV ORIENTDB_ROOT_PASSWORD root


# Add the application resources URL
RUN echo "deb http://archive.ubuntu.com/ubuntu/ trusty main universe" >> /etc/apt/sources.list
RUN apt-get update

# Install basic applications
RUN apt-get install -y --force-yes tar git curl vim wget dialog net-tools build-essential 


# Crossbar.io connection defaults
ENV CBURL ws://crossbar:8080/ws
ENV CBREALM realm1

# install Autobahn|Python
RUN pip install -U pip && pip install autobahn[twisted] && pip install crossbar

# Install basic applications
RUN apt-get install -y --force-yes tar git curl vim wget dialog net-tools build-essential 

# Install Python and Basic Python Tools
RUN apt-get install -y --force-yes --force-yes python python-dev python-distribute python-pip



RUN apt-get update && apt-get -y --force-yes install python-numpy \
    python-pandas


# Install dependancies
RUN pip install --upgrade pip
RUN pip install cython
RUN pip install simplejson

RUN pip install daff networkx path.py


RUN  apt-get -yq update && \
     apt-get -yqq install ssh
RUN apt-get install -y --force-yes python-h5py

RUN apt-get update


WORKDIR /app


