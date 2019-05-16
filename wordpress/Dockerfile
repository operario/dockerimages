FROM wordpress

MAINTAINER Operar "ola@operar.io"

RUN apt-get update && apt-get install -q -y ssmtp mailutils && rm -rf /var/lib/apt/lists/*

RUN echo "hostname=localhost.localdomain" > /etc/ssmtp/ssmtp.conf
RUN echo "root=ola@operar.io" >> /etc/ssmtp/ssmtp.conf
RUN echo "mailhub=maildev" >> /etc/ssmtp/ssmtp.conf
RUN echo "upload_max_filesize = 15M" > /usr/local/etc/php/conf.d/realskeptic-php-ext.ini
RUN echo "post_max_size = 15M" >> /usr/local/etc/php/conf.d/realskeptic-php-ext.ini
RUN echo "localhost localhost.localdomain" >> /etc/hosts
