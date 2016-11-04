FROM            mysql:5.7

MAINTAINER      Masaharu.I

COPY            ./my.cnf /etc/mysql/

RUN             apt-get update && apt-get install -y zsh vim wget

EXPOSE          3306

CMD             ["mysqld"]
