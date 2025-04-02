# https://hub.docker.com/_/php
# FROM php:8.2-apache
FROM php:8.2-fpm

RUN apt-get update && \
    docker-php-ext-install \
     mysqli \ 
     pdo 


RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd
  

  


