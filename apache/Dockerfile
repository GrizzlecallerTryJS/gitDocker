FROM php:7.2-apache


# PHP extensions
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng-dev \ 
    && pecl install xdebug \
    && docker-php-ext-install -j$(nproc) mbstring pdo_mysql tokenizer iconv mysqli \ 
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-enable xdebug \
    && pecl install mcrypt-1.0.2 \
    && docker-php-ext-enable mcrypt
# Apache modules
RUN a2enmod rewrite