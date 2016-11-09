FROM php:7.0-apache
RUN apt-get update && apt-get install -y git 
RUN useradd framadate && \
    mkdir /var/www/framadate && \
    cd /var/www/framadate && \
    git clone --branch 1.0.2 https://framagit.org/framasoft/framadate.git .

WORKDIR /var/www/framadate

RUN apt-get install -y php5-intl
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer update && composer install
