FROM docker.io/php:7.1.8-fpm
# 更新apt-get源 使用aliyun的源
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak && \
	echo "deb http://mirrors.aliyun.com/debian wheezy main contrib non-free" >/etc/apt/sources.list && \
	echo "deb-src http://mirrors.aliyun.com/debian wheezy main contrib non-free" >>/etc/apt/sources.list && \
	echo "deb http://mirrors.aliyun.com/debian wheezy-updates main contrib non-free" >>/etc/apt/sources.list && \
	echo "deb-src http://mirrors.aliyun.com/debian wheezy-updates main contrib non-free" >>/etc/apt/sources.list && \
	echo "deb http://mirrors.aliyun.com/debian-security wheezy/updates main contrib non-free" >>/etc/apt/sources.list && \
	echo "deb-src http://mirrors.aliyun.com/debian-security wheezy/updates main contrib non-free" >>/etc/apt/sources.list
# 安装php扩展
RUN apt-get update && apt-get install -y \
        libmcrypt-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt pdo_mysql bcmath mysqli
