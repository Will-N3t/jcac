FROM jenkins/jenkins:2.346.2

LABEL maintainer="ewe@praqma.net"
COPY plugins_extra.txt /usr/share/jenkins/ref/plugins_extra.txt

ENV JENKINS_HOME /var/jenkins_home

ARG JAVA_OPTS
ENV JAVA_OPTS "-Djenkins.install.runSetupWizard=false ${JAVA_OPTS:-}"

RUN jenkins-plugin-cli --plugin-file /usr/share/jenkins/ref/plugins_extra.txt --plugins delivery-pipeline-plugin:1.3.2 deployit-plugin