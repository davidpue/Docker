FROM ubuntu:12.04

MAINTAINER David Puehringer Version: 0.1

RUN apt-get update && apt-get install -y apache2

RUN rm /var/www/index.html
RUN echo "Hallo ich bin ein Apache Container der mit einem Dockerfile erstellt wurde" > /var/www/index.html

env APACHE_RUN_USER    www-data
env APACHE_RUN_GROUP   www-data
env APACHE_PID_FILE    /var/run/apache2.pid
env APACHE_RUN_DIR     /var/run/apache2
env APACHE_LOCK_DIR    /var/lock/apache2
env APACHE_LOG_DIR     /var/log/apache2
env LANG               C

EXPOSE 80

CMD ["apache2", "-D", "FOREGROUND"]