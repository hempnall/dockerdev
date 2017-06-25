FROM nginx
RUN apt-get -y update && apt-get -y install nano apache2-utils
COPY index.html /usr/share/nginx/html
RUN mkdir -p /usr/share/nginx/html/dev
RUN mkdir -p /usr/share/nginx/html/stg
RUN mkdir -p /usr/share/nginx/html/prd
RUN mkdir -p /etc/nginx/conf.d
RUN echo "I'm development" > /usr/share/nginx/html/dev/index.html
RUN echo "I'm staging" > /usr/share/nginx/html/stg/index.html
RUN echo "I'm production" > /usr/share/nginx/html/prd/index.html
COPY etc/nginx/dot_htpasswd /etc/nginx/dot_htpasswd
COPY etc/nginx/conf.d/* /etc/nginx/conf.d
RUN rm /etc/nginx/conf.d/default.conf


