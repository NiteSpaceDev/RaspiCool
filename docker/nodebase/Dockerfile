FROM resin/rpi-raspbian:latest
ENTRYPOINT []

RUN apt-get update && \
    apt-get -qy install curl build-essential python ca-certificates
WORKDIR /root/
RUN curl -O http://nodejs.org/dist/v10.4.0/node-v10.4.0-linux-armv7l.tar.gz 
RUN tar -xvf node-*.tar.gz -C /usr/local --strip-components=1

CMD ["node"]
