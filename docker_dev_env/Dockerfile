#
# Ubuntu Dockerfile
#
# https://github.com/dockerfile/ubuntu
#

# Pull base image.
FROM ubuntu:18.04

# Install.
RUN \
  apt-get update && \
  apt-get install -y sudo && \
  apt-get install -y build-essential && \
  apt-get install -y curl git vim wget cmake

RUN \
  apt-get install -y libssl-dev libcurl4-openssl-dev zlib1g-dev libcpprest-dev

# Add User samuel, set passwd to samuel
RUN useradd -m samuel && echo "samuel:samuel" | chpasswd && adduser samuel sudo

USER samuel

WORKDIR /home/samuel/Github/huobi_Cpp

# Define default command.
CMD ["bash"]
