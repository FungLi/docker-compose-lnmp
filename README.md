docker-compose-lnmp
==================

1、目录结构：
-------

```sh
├── docker-compose
│   ├── mysql
│   │   └── docker-compose.yml
│   └── nginx-php
│       ├── docker-compose.yml
│       └── php
│           └── Dockerfile
├── etc
│   ├── mysql
│   │   ├── docker.cnf
│   │   └── mysql.cnf
│   ├── nginx
│   │   └── default.conf
│   └── php
│       └── php.ini
├── logs
│   └── nginx
│       ├── access.log
│       └── error.log
├── README.md
└── www
    ├── index.html
    └── index.php
```

- ##### docker-compose 目录
  docker-compose.yml和Dockerfile文件目录
- ##### etc 目录
  mysql、nginx、php 的配置文件目录，会挂载到容器中
- ##### logs 目录
  文件日志目录，用于存储nginx等应用的一些日志文件
- ##### www 目录
  站点目录，会挂在到php-fpm容器中
