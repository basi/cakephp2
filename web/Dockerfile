FROM php:5.6-apache
MAINTAINER docker-web

RUN apt-get update \
    && apt-get -y install vim wget cron lsb-release libicu-dev mysql-client \
    && docker-php-ext-install pdo_mysql mysqli intl
RUN ln -s /etc/apache2/mods-available/rewrite.load /etc/apache2/mods-enabled/rewrite.load
RUN ln -s /etc/apache2/mods-available/vhost_alias.load /etc/apache2/mods-enabled
RUN echo ServerName $HOSTNAME > /etc/apache2/conf-available/fqdn.conf && a2enconf fqdn
RUN a2enmod headers
RUN a2enmod include

COPY ./apache2.conf /etc/apache2/apache2.conf

COPY ./localhost.conf /etc/apache2/sites-available/000-default.conf

COPY ./php.ini /usr/local/etc/php/
