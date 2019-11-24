ARG ELK_VERSION

# https://github.com/elastic/beats/tree/master/filebeat
FROM docker.elastic.co/beats/filebeat:${ELK_VERSION}

# Copy our custom configuration file - see https://medium.com/@bcoste/powerful-logging-with-docker-filebeat-and-elasticsearch-8ad021aecd87
COPY ./personalised_filebeat.yml /usr/share/filebeat/filebeat.yml

#USER root
# Create a directory to map volume with all docker log files
#RUN mkdir /usr/share/filebeat/dockerlogs
#RUN chown -R root /usr/share/filebeat/
#RUN chmod -R go-w /usr/share/filebeat/

# Add your filebeat plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
