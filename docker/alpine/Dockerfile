FROM alpine
MAINTAINER Anastas Dancha <anapsix@random.io>
RUN apk upgrade --update && \
    apk add apk add alpine-sdk php-dev php-cli php-pear
    pecl install mongo && \
    echo "extension=mongo.so" >> /etc/php5-cli/php.ini && \
    apt del --purge alpine-sdk php5-dev php-pear
ADD . /rockmongo
WORKDIR /rockmongo
EXPOSE 5000
CMD ["php -S 0.0.0.0:5000"]
