FROM ubuntu:19.04

RUN cd /tmp \
  && apt-get update \
  && apt-get install -y wget \
  && wget https://artifacts-openshift-master.svc.ci.openshift.org/zips/openshift-origin-client-tools-v4.0.0-alpha.0-c68d654-1950-linux-64bit.tar.gz \
  && tar -xvzf openshift-origin-client-tools-v4.0.0-alpha.0-c68d654-1950-linux-64bit.tar.gz \
  && mv openshift-origin-client-tools-v4.0.0-alpha.0-c68d654-1950-linux-64bit/oc /usr/local/bin/ \
  && rm -rf openshift-origin-client-tools-v4.0.0-alpha.0-c68d654-1950-linux-64bit openshift-origin-client-tools-v4.0.0-alpha.0-c68d654-1950-linux-64bit.tar.gz

ENTRYPOINT ["oc"]

CMD ["help"]
