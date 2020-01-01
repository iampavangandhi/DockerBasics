#Step1
FROM alpine

#Step2 : install Soft
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/main' >> /etc/apk/repositories
RUN echo 'http://dl-cdn.alpinelinux.org/alpine/v3.6/community' >> /etc/apk/repositories

RUN apk update
RUN apk add mongodb
RUN apk add binutils

#Step2.5 : Configure Soft
VOLUME [ "/data/db" ]
WORKDIR /data
EXPOSE 27017

#Step3 : Set Default CMDs
CMD [ "mongod" ]
