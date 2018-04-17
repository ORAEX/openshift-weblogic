FROM registry.access.redhat.com/rhel7:latest
MAINTAINER Johnathan Kupferer <jkupfere@redhat.com>

ENV JAVA_VERSION=${JAVA_VERSION:-1.8.0} \
    JAVA_TYPE=${JAVA_TYPE:-openjdk}

ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk

RUN yum --disablerepo=* \
        --enablerepo=rhel-7-server-rpms \
        --enablerepo=rhel-7-server-extras-rpms \
        --enablerepo=rhel-7-server-optional-rpms \
        --enablerepo=rhel-7-server-thirdparty-oracle-java-rpms \
      install -y \
      java-1.8.0-openjdk-devel \
      java-1.8.0-openjdk && \
    yum clean all
