FROM amazonlinux:1

RUN yum install -y php73 php73-cli php73-common php73-soap php73-json php73-mbstring php73-mysqlnd php73-pdo php73-process php73-xml httpd24 httpd24-tools openssl zip unzip php73-zip git

RUN yum install -y nano
RUN yum install -y vim

RUN  curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer


RUN mkdir -p /var/www/html
RUN chmod -R 755 /var/www/html

ADD v-host.conf /etc/httpd/conf.d

WORKDIR /var/www/html

# COPY composer.json .
# COPY composer.lock .
# RUN composer install

EXPOSE 80
EXPOSE 443

CMD /usr/sbin/httpd -DFOREGROUND
