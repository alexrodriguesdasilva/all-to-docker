#docker build -t alexrodriguesdasilva/no-root-my-website:1.0.0 .
#docker run -d -p 80:80 --name no-root-my-website alexrodriguesdasilva/no-root-my-website:1.0.0

FROM nginx

LABEL version="1.0.0" \
      description="Providing website with NGINX" \
      maintainer="Alex Rodrigues da Silva <alex_horo@hotmail.com>"

COPY ./site/index.html /usr/share/nginx/html/

EXPOSE 80

WORKDIR /usr/share/nginx/html/

ENTRYPOINT ["/usr/sbin/nginx"]

CMD ["-g", "daemon off;"]

RUN groupadd -g 999 appuser && \          
    useradd -r -u 999 -g appuser appuser && \
    chown -R appuser:appuser /etc/nginx/ /var/log/nginx/ /var/cache/nginx/ /var/run/

USER appuser