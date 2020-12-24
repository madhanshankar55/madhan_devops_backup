FROM python:3.6-alpine

#ARG CURATOR_VERSION 

#RUN pip install elasticsearch-curator==$(CURATOR_VERSION) &&\ rm -rf /var/cache/apk/*
RUN apk --no-cache add python py-setuptools py-pip gcc libffi py-cffi python-dev libffi-dev py-openssl musl-dev linux-headers openssl-dev libssl1.0 && \ pip install elasticsearch-curator==5.8.1

COPY ./config/ /config

RUN /usr/bin/crontab /config/crontab.txt

CMD ["/usr/sbin/crond","-f"]
