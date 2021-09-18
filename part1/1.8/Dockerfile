FROM ubuntu:18.04
WORKDIR /usr/src/app
RUN apt-get update && apt-get -y install curl
COPY script.sh .
CMD  ./script.sh
