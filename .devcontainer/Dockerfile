FROM php:8.0.2-apache

RUN apt-get update && apt-get install -y libzip-dev zlib1g-dev \
  && docker-php-ext-install zip \
  && apt-get clean

ENV APACHE_DOCUMENT_ROOT /var/www/myapp/html
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf \
  && sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

# https://qiita.com/yatsbashy/items/02bbbebbfe7e5a5976bc を参考に、composerイメージからバイナリを取得。
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
