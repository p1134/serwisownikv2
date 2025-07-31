FROM php:8.2-fpm

WORKDIR /var/www/html

RUN apt update && apt install -y git unzip curl zip libicu-dev libonig-dev libxml2-dev \
    && docker-php-ext-install intl pdo pdo_mysql

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

CMD ["php-fpm"]