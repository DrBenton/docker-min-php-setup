FROM php:7-fpm

# PHP additional extensions build & install
RUN apt-get update && apt-get install -y \
    libsqlite3-dev \
    libicu-dev

RUN docker-php-ext-install \
    mbstring \
    pdo \
    pdo_mysql \
    pdo_sqlite \
    intl

