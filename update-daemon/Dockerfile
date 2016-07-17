FROM php:7-cli
RUN apt-get update && apt-get install -y libpq-dev && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-install -j$(nproc) pgsql opcache pcntl
WORKDIR /srv/http/tt-rss
ENTRYPOINT ["/usr/local/bin/php","./update_daemon2.php"]
USER 1000
