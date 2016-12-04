FROM debian:jessie

MAINTAINER Jeff Jacquelot <jacquelotjeff@gmail.com>

RUN apt-get update && apt-get install -y nginx
RUN rm -rf /tmp/*

ADD config/nginx.conf /etc/nginx/
ADD config/project.conf /etc/nginx/conf.d/

RUN echo "upstream php-upstream { server php:9001; }" > /etc/nginx/conf.d/upstream.conf

CMD ["nginx"]

EXPOSE 80
EXPOSE 443
