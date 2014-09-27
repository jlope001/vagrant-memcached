FROM       centos:centos7
MAINTAINER Jose Lopez "jlope001@gmail.com"

# Enable additional repositories
RUN yum -y install memcached

EXPOSE 11211

ADD ./scripts/startup.sh /opt/startup.sh
CMD ["/bin/bash", "/opt/startup.sh"]
