#docker build -t alexrodriguesdasilva/my-website:1.0.0 .
#docker run -d -p 80:80 --name my-website alexrodriguesdasilva/my-website:1.0.0

FROM nginx

LABEL version="1.0.0" \
      description="Providing website with NGINX" \
      maintainer="Alex Rodrigues da Silva <alex_horo@hotmail.com>"

COPY ./site/index.html /usr/share/nginx/html/

EXPOSE 80

WORKDIR /usr/share/nginx/html/

ENTRYPOINT ["/usr/sbin/nginx"]

CMD ["-g", "daemon off;"]