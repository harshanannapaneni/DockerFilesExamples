#Using openjdk image from dockerhub.
FROM openjdk:17

# Metadata for the docker image.
LABEL env=production\
maintainer="Harsha Nannapaneni harshanannapaneni10@gmail.com"\
description="This is a simple dockerfile that runs jenkins in openjdk image"

# Defining enviroment variable: apparea to define root directory for data to reside.
ENV apparea /data/app
ENV JENKINS_PORT 8080

# Creating the directory structure /data/app.
RUN mkdir -p $apparea 

ADD https://get.jenkins.io/war-stable/2.452.2/jenkins.war ${apparea}

# Exposing the port 8080 for jenkins.
EXPOSE $JENKINS_PORT

# Working directory
WORKDIR $apparea

# Running jenkins
CMD ["java", "-jar", "jenkins.war"]