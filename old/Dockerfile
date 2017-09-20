FROM php:5.6.24-fpm
RUN apt-get update
RUN apt-get install -y libyaml-dev && pecl install yaml && docker-php-ext-enable yaml
RUN pecl install redis-2.2.8 && docker-php-ext-enable redis
RUN docker-php-ext-install pdo_mysql
RUN apt-get install -y libmcrypt-dev && docker-php-ext-install -j$(nproc) mcrypt
RUN pecl install xdebug && docker-php-ext-enable xdebug \
    && echo "xdebug.remote_enable=on" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
    && echo "xdebug.remote_autostart=off" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini \
