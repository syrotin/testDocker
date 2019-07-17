FROM ubuntu:latest

RUN apt update
RUN apt install nano apache2 -y
ENV TZ=Europe/Kiev
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt install php  libapache2-mod-php -y

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_USER www-data

EXPOSE 80

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
