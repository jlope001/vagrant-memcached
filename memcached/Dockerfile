FROM       centos:centos6
MAINTAINER Jose Lopez "jlope001@gmail.com"

# Enable additional repositories
RUN rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum -y update

RUN yum -y install memcached

EXPOSE 11211

ADD ./scripts/startup.sh /opt/startup.sh
CMD ["/bin/bash", "/opt/startup.sh"]
