FROM ubuntu
RUN apt-get update \
    && echo "mysql-server mysql-server/root_password password password" | debconf-set-selections \
    && echo "mysql-server mysql-server/root_password_again password password" | debconf-set-selections \
    && apt-get install -y tzdata apache2 vim php7.0 libapache2-mod-php mysql-client telnet mysql-server php-mysql \
    && cp -p /usr/share/zoneinfo/Asia/Chongqing /etc/localtime \
    && usermod -d /var/lib/mysql mysql \
    && chown -R mysql:mysql /var/lib/mysql
EXPOSE 80
ENTRYPOINT ["/bin/bash"]
