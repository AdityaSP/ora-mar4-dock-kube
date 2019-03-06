FROM alpine:3.9
RUN apk update
RUN apk add apache2

COPY docker-entrypoint.sh /bin
RUN chmod +x /bin/docker-entrypoint.sh
ENV APACHE_PORT 80
ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["httpd", "-D", "FOREGROUND"]

# docker-entrypoint.sh httpd -D FOREGROUND
