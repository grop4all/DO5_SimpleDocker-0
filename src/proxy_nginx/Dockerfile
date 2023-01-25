FROM nginx:1.22.1

COPY ./proxy_nginx_conf.d/nginx.conf /etc/nginx/conf.d/nginx.conf

RUN rm /etc/nginx/conf.d/default.conf 

CMD ["nginx", "-g", "daemon off;"]