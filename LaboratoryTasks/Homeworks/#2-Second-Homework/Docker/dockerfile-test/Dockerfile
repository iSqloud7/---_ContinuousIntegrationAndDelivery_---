FROM ubuntu:18.04
LABEL maintainer="ivanpupinoski03@gmail.com"
RUN apt-get update; apt-get install -y apache2
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2
COPY . /var/www/
EXPOSE 80
ENTRYPOINT ["/usr/sbin/apachectl']
CMD ["-D", "FOREGROUND"]