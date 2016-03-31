FROM php:7-fpm

# PHP additional extensions build & install
RUN apt-get update && apt-get install -y \
    libsqlite3-dev \
    libicu-dev \
    zlib1g-dev

RUN docker-php-ext-install \
    mbstring \
    pdo \
    pdo_mysql \
    pdo_sqlite \
    intl \
    zip

# Composer install
RUN php -r "readfile('https://getcomposer.org/installer');" | php
RUN mv composer.phar /usr/local/bin/composer
RUN chmod +x /usr/local/bin/composer

# Misc additional tools install
RUN apt-get install -y git

