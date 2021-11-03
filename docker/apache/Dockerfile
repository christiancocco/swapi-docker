FROM php:7.4-apache

RUN apt-get update \
&& apt-get install -y \
&& apt-get autoremove -y \
&& docker-php-ext-install mysqli pdo pdo_mysql \
&& apt-get install curl -y \
&& apt-get install git -y\
&& apt-get install zip -y\
&& curl -fsSL https://deb.nodesource.com/setup_current.x | bash - \
&& apt-get install -y nodejs

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html/swapi-docker/

EXPOSE 8050
