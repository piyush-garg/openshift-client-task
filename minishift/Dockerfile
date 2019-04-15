FROM docker.io/centos:7

RUN cd /tmp \
  && yum -y update \
  && yum install -y wget \
  && wget https://github.com/openshift/origin/releases/download/v3.11.0/openshift-origin-client-tools-v3.11.0-0cbc58b-linux-64bit.tar.gz \
  && tar -xvzf openshift-origin-client-tools-v3.11.0-0cbc58b-linux-64bit.tar.gz \
  && mv openshift-origin-client-tools-v3.11.0-0cbc58b-linux-64bit/oc /usr/local/bin/ \
  && rm -rf openshift-origin-client-tools-v3.11.0-0cbc58b-linux-64bit openshift-origin-client-tools-v3.11.0-0cbc58b-linux-64bit.tar.gz

ENTRYPOINT ["oc"]

CMD ["help"]
