FROM ubuntu
RUN apt update

ARG DEBIAN_FRONTEND=noninteractive
RUN apt install apache2 -y
RUN apt install apache2-utils -y
RUN apt clean

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80
CMD ["apache2ctl", "-D", "FOREGROUND"]
