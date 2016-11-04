FROM            centos:6.6

MAINTAINER      Masaharu.I

RUN             rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm && \
                rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-6.rpm && \
                rpm -Uvh http://dev.mysql.com/get/mysql-community-release-el6-5.noarch.rpm
RUN             yum update -y; yum clean all
RUN             yum install -y httpd wget git tig zip gcc make httpd-devel openssl-devel openssh-clients openssh-server; yum clean all
RUN             yum install -y --enablerepo=remi-php56 install php php-opcache php-devel php-mbstring php-mcrypt php-mysqlnd php-phpunit-PHPUnit php-pecl-xdebug php-pecl-xhprof; yum clean all
RUN             chkconfig httpd on


EXPOSE          80

CMD             ["/usr/sbin/apachectl", "-D", "FOREGROUND"]
