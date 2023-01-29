FROM nginx:1.22.1


COPY ./nginx/nginx.conf /etc/nginx/conf.d/nginx.conf

WORKDIR /usr/src/app
COPY ./server/main.c  .
COPY ./start-server.sh .

RUN \
    useradd user1 && \
    apt-get update && \
    apt-get install -y gcc && \
    apt-get install -y libfcgi-dev && \
    apt-get install -y spawn-fcgi && \
    rm /etc/nginx/conf.d/default.conf && \
    rm -rf /var/lib/apt/lists/* && \
    chmod 755 start-server.sh 

# USER user1

HEALTHCHECK --interval=1m --timeout=3s \
  CMD curl -f http://localhost:81 || exit 1

ENTRYPOINT ["./start-server.sh"]

                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   