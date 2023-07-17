FROM ubuntu:focal
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get install -y apache2  \
    && apt-get install -y git
#RUN git clone https://github.com/jhyun0913/static-web-tamplate.git
#RUN cp -r static-web-tamplate/* /var/www/html/
RUN git clone https://github.com/jhyun0913/test_page.git
RUN cp -r test_page/* /var/www/html/
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
EXPOSE 80
