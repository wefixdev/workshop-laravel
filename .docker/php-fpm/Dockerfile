FROM php:7.3.9-fpm-alpine3.9

RUN apk add mysql-client
RUN docker-php-ext-install pdo pdo_mysql
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www
RUN rm -Rf /var/www/html
RUN ln -s public html

EXPOSE 9000
ENTRYPOINT ["php-fpm"]

