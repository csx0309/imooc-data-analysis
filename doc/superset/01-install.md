###  安装
- add docker-compose.yml
``` yml
version: "3"
services:
   superset:
     image: amancevice/superset
     ports:
       - "8888:8888"
   db:
     image: mysql:5.7
     volumes:
       - ./data:/var/lib/mysql
     restart: always
     ports:
       - "3306:3306"
     environment:
       MYSQL_ROOT_PASSWORD: password
       MYSQL_DATABASE: imooc
       MYSQL_USER: root
       MYSQL_PASSWORD: 111111

```


``` bash
docker-compose up

```