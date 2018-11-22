FROM php:7.1-fpm

RUN apt-get update
RUN apt install -y curl git zip

RUN mkdir /app
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer

ADD php.ini /usr/local/etc/php/conf.d/40-custom.ini

WORKDIR /app

CMD ["php-fpm"]