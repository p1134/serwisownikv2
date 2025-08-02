FROM php:8.2-fpm

# Zależności systemowe
RUN apt-get update && apt-get install -y \
    git unzip curl libicu-dev libpq-dev libzip-dev zip \
    && docker-php-ext-install intl pdo pdo_pgsql opcache zip

# Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
