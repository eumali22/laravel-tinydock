FROM php:8.0-fpm-alpine

# install modules
RUN docker-php-ext-install opcache bcmath
COPY php/production/opcache.ini /usr/local/etc/php/conf.d/opcache.ini

# install composer
COPY --from=composer/composer /usr/bin/composer /usr/bin/composer

# create group www and user www
RUN addgroup -S www && adduser -S www -G www

# copy files from current directory to /var/www/html/public of container
COPY ./public /var/www/html/public

# copy permissions
COPY --chown=www:www . /var/www/html

# switch to created user
USER www
