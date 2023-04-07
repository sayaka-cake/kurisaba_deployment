FROM php:5.6-apache

RUN apt-get update && \
    docker-php-ext-install mysqli pdo pdo_mysql

# TODO: mkdir tmp
RUN mkdir -p /var/www/html/tmp/dwoo
RUN chown www-data:www-data /var/www/html/tmp/dwoo
RUN chmod 777 /var/www/html/tmp/dwoo


RUN a2enmod rewrite
#
#RUN sed -i '/LoadModule rewrite_module/s/^#//g' /usr/local/apache2/conf/httpd.conf
#
#RUN { \
#  echo 'IncludeOptional conf.d/*.conf'; \
#} >> /usr/local/apache2/conf/httpd.conf \
#  && mkdir /usr/local/apache2/conf.d