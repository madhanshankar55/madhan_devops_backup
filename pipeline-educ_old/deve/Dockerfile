FROM logstash:7.6.2
USER logstash

COPY pipeline/ /usr/share/logstash/pipeline/
COPY logstash.yml /usr/share/logstash/config/logstash.yml

USER root
RUN rm -rf /usr/share/logstash/pipeline/logstash.conf
RUN chown -R logstash /usr/share/logstash/pipeline/*