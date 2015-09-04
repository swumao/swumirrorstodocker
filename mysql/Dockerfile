FROM ubuntu:12.04
## 备份镜像列表
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak

## 更换为mirrors.swu.edu.cn的镜像

RUN echo "deb http://mirrors.swu.edu.cn/ubuntu/ precise main restricted universe multiverse\n\
deb http://mirrors.swu.edu.cn/ubuntu/ precise-security main restricted universe multiverse\n\
deb http://mirrors.swu.edu.cn/ubuntu/ precise-updates main restricted universe multiverse\n\
deb http://mirrors.swu.edu.cn/ubuntu/ precise-proposed main restricted universe multiverse\n\
deb http://mirrors.swu.edu.cn/ubuntu/ precise-backports main restricted universe multiverse" >> /etc/apt/sources.list

## 安装软件
RUN apt-get update && apt-get install -y mysql-server mysql-client

EXPOSE 3306

COPY config/mysql.cnf /etc/mysql/mysql.cnf

CMD /usr/sbin/mysqld