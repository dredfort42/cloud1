FROM debian:buster

RUN apt-get update -y 
RUN apt-get install mariadb-server -y
COPY ./mariadb.conf ./etc/mysql/mariadb.conf.d/50-server.cnf
COPY ./setup.sql ./setup.sql
RUN service mysql start && mysql < ./setup.sql
RUN rm ./setup.sql

EXPOSE 3306

CMD /usr/bin/mysqld_safe