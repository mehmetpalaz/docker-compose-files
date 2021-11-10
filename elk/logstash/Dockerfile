ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELK_VERSION}

COPY ojdbc6.jar /usr/share/logstash/logstash-core/lib/jars/ojdbc6.jar
COPY ojdbc7.jar /usr/share/logstash/logstash-core/lib/jars/ojdbc7.jar
COPY query.sql /usr/share/logstash/data/query.sql