FROM php:8.0.2-fpm-alpine3.12

RUN addgroup -g 1000 laravel && adduser -G laravel -g laravel -s /bin/sh -D laravel 

WORKDIR /var/www/html
# RUN docker-php-ext-install pdo pdo_mysql bcmath

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
# BC Math
RUN install-php-extensions bcmath pdo pdo_mysql 

RUN chown laravel:laravel /var/www/html 