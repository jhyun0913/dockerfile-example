FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get install -y nginx git
RUN git clone https://github.com/jhyun0913/test_page.git
COPY nginx/sites-available/default /etc/nginx/sites-available/default
RUN cp -r test_page/* /usr/share/nginx/html/
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80
