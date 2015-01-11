FROM ubuntu:12.04

MAINTAINER ruslanloman version: 0.1

RUN apt-get update && apt-get install git vim wget curl -y
RUN release=$(awk -F "=" '/DISTRIB_CODENAME=/ {print $2}' /etc/lsb-release) && wget https://apt.puppetlabs.com/puppetlabs-release-${release}.deb -O /tmp/puppetlabs-release-${release}.deb && dpkg -i /tmp/puppetlabs-release-${release}.deb
RUN apt-get update && apt-get install puppet vim-puppet -y
RUN vim-addons install puppet
RUN apt-get clean
RUN rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*
