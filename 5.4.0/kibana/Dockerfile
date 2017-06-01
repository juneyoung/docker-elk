FROM centos
MAINTAINER juneyoung <juneyoung@hanmail.net>

ARG u=kibana
ARG uid=1000
ARG g=kibana
ARG gid=1000
ARG p=kibana

# add USER
RUN groupadd -g ${gid} ${g}
RUN useradd -d /home/${u} -u ${uid} -g ${g} -s /bin/bash ${u} 

# yum settings
RUN yum -y update
RUN yum -y install java-1.8.0-openjdk.x86_64
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.131-3.b12.el7_3.x86_64/jre/

# install wget
RUN yum install -y wget

CMD ["/usr/sbin/init"]
