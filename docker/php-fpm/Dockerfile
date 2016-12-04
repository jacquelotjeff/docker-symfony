FROM php:7.0-fpm

MAINTAINER Jeff Jacquelot <jacquelotjeff@gmail.com>

RUN rm -rf /tmp/*

ADD config/project.ini /etc/php/7.0/fpm/conf.d/
ADD config/project.ini /etc/php/7.0/cli/conf.d/

ADD config/project.pool.conf /etc/php/7.0/fpm/pool.d/

CMD ["php-fpm", "-F"]

EXPOSE 9000
