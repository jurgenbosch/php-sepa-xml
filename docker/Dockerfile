FROM php:8.1-fpm

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    cron \
    curl \
    git \
    gnupg2 \
    openssl \
    screen \
    unzip \
    vim  \
    zip  \
    zlib1g-dev

RUN docker-php-ext-configure pcntl --enable-pcntl && \
    docker-php-ext-install pcntl \
    pdo_mysql \
    bcmath

RUN curl -s https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer && \
    composer about && \
    composer self-update
