FROM ubuntu:14.04
ENV TERM=xterm
LABEL "purpose"="learn-docker"
RUN apt-get update
RUN apt-get install apache2 -y
ADD index.html /var/www/html
WORKDIR /var/www/html
RUN ["/bin/bash","-c","echo hello >> test.html"]
EXPOSE 80
CMD apachectl -DFOREGROUND