FROM jenkins/jenkins:2.150.1
MAINTAINER OME

# Temp fix robot test results
ENV JAVA_OPTS "-Dhudson.model.DirectoryBrowserSupport.CSP="

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/plugins.sh /usr/share/jenkins/ref/plugins.txt

USER root
RUN chown -R jenkins:jenkins /var/jenkins_home
VOLUME /var/jenkins_home
