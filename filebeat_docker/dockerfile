FROM docker.elastic.co/beats/filebeat:7.6.2
COPY filebeat.yml /usr/share/filebeat/filebeat.yml
USER root
RUN chmod 744 /usr/share/filebeat/filebeat.yml
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
USER root
