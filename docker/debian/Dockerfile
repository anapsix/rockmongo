FROM debian
MAINTAINER Anastas Dancha <anapsix@random.io>
RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -qqy php5-dev php5-cli php-pear && \
    pecl install mongo && \
    echo "extension=mongo.so" >> /etc/php5/cli/php.ini && \
    apt-get purge -y php5-dev php-pear
ADD . /rockmongo
WORKDIR /rockmongo
EXPOSE 5000
CMD php -S 0.0.0.0:5000
