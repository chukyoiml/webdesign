FROM php:8.1-apache

RUN apt-get update && \
    apt-get install -y libonig-dev && \
    apt-get install -y default-libmysqlclient-dev && \
    docker-php-ext-install pdo_mysql mysqli

COPY vhost.conf /etc/apache2/sites-available/000-default.conf

RUN a2enmod rewrite
