FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get install -y nginx git
RUN git clone https://github.com/jhyun0913/test_page.git
RUN cp -r test_page/* /var/www/html/
COPY nginx/sites-available/default /etc/nginx/sites-available/default
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80
