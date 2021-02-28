FROM php:8.0.2-fpm-alpine3.12


RUN apk --no-cache add shadow && usermod -u 1000 www-data
RUN docker-php-ext-install pdo pdo_mysql bcmath