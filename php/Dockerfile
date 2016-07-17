FROM php:7-fpm
RUN apt-get update && apt-get install -y libpq-dev && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-install -j$(nproc) pgsql opcache
