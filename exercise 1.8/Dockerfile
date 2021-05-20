FROM ubuntu:18.04
WORKDIR /usr/src/app
COPY script.sh .
RUN chmod +x script.sh
RUN apt-get update
RUN apt-get install curl wget -y
CMD ./script.sh