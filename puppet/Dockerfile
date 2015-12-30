FROM ubuntu:14.04

MAINTAINER ruslanloman version: 0.1

RUN apt-get update && apt-get install git vim wget curl -y; \
    release=$(awk -F "=" '/DISTRIB_CODENAME=/ {print $2}' /etc/lsb-release); \
    wget https://apt.puppetlabs.com/puppetlabs-release-${release}.deb -O /tmp/puppetlabs-release-${release}.deb; \
    dpkg -i /tmp/puppetlabs-release-${release}.deb; \
    apt-get update; apt-get install puppet vim-puppet -y; \
    vim-addons install puppet; gem install deep_merge; \
    apt-get clean; \
    rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*
