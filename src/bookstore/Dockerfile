FROM php:7.3-apache

RUN apt update
RUN apt -y install git libpq-dev

RUN docker-php-ext-install pgsql pdo pdo_pgsql

RUN git clone https://pubgit.postgrespro.ru/pub/dev1app.git /var/www/html
COPY config.php /var/www/html/config.php
