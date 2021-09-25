FROM php:7.4-fpm-alpine
RUN apk add --update --no-cache \
        bash \
        yarn 
RUN docker-php-ext-install pdo_mysql
COPY --from=composer /usr/bin/composer /usr/bin/composer
WORKDIR /var/www
CMD ["php-fpm"]
EXPOSE 9000
