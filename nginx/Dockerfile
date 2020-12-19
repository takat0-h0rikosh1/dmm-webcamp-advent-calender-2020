FROM nginx:alpine

RUN rm -f /etc/nginx/conf.d/*

ADD nginx.conf.template /etc/nginx/conf.d/nginx.conf.template

ENV SERVER_HOST localhost

CMD envsubst \
    '$$SERVER_HOST' \
    < /etc/nginx/conf.d/nginx.conf.template > \
    /etc/nginx/conf.d/nginx.conf \
    && nginx -g 'daemon off;'

