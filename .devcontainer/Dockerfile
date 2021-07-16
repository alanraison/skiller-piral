FROM node:14

ARG USERNAME=node
ARG USER_UID=1000
ARG USER_GID=${USER_UID}
# TODO: create user if they don't exist.

RUN apt-get update \
  && apt-get upgrade -y \
  && apt-get install -y --no-install-recommends \
    sudo \
  && echo "${USERNAME}  ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/node \
  && chmod 0400 /etc/sudoers.d/node
  
