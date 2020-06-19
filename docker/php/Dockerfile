FROM php:7.3.8-apache
# install composer
RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
&& apt-get install -y \
git \
zip \
unzip \
vim

RUN apt-get update \
    && apt-get install -y libpq-dev \
    && docker-php-ext-install pdo_mysql pdo_pgsql
RUN pecl install xdebug \
  && docker-php-ext-enable xdebug

RUN apt-get -y install libzip-dev
RUN docker-php-ext-install zip

WORKDIR /var/www/html