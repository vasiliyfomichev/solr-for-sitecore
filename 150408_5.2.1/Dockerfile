FROM    java:8
MAINTAINER  Vasiliy Fomichev "vasya.fomichev@gmail.com"

ENV SOLR_VERSION 5.2.1
ENV SOLR solr-$SOLR_VERSION
ENV SOLR_USER solr
ENV CORE_NAME itembuckets
ENV SOLR_PATH /opt/$SOLR/server/solr

RUN export DEBIAN_FRONTEND=noninteractive && \
  apt-get update && \
  apt-get -y install \
    curl \
    lsof \
    procps && \
  groupadd -r $SOLR_USER && \
  useradd -r -g $SOLR_USER $SOLR_USER && \
  mkdir -p /opt && \
  wget -nv --output-document=/opt/$SOLR.tgz http://www.us.apache.org/dist/lucene/solr/$SOLR_VERSION/$SOLR.tgz && \
  tar -C /opt --extract --file /opt/$SOLR.tgz && \
  rm /opt/$SOLR.tgz && \
  ln -s /opt/$SOLR /opt/solr && \
  chown -R $SOLR_USER:$SOLR_USER /opt/solr /opt/$SOLR

RUN cp -af $SOLR_PATH/configsets/basic_configs $SOLR_PATH/$CORE_NAME
COPY schema.xml $SOLR_PATH/$CORE_NAME/conf/
RUN echo name=$CORE_NAME > $SOLR_PATH/$CORE_NAME/core.properties


EXPOSE 8983
WORKDIR /opt/solr
USER $SOLR_USER
CMD ["/bin/bash", "-c", "/opt/solr/bin/solr -f"]