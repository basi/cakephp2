# docker_cakephp2

## docker for mac
https://docs.docker.com/docker-for-mac/install/

## setup
```
$ git clone git@github.com:basi/docker_cakephp2.git
$ cd docker_cakephp2/www/
$ git clone -b 2.x git://github.com/cakephp/cakephp.git
$ cd ../
$ docker-compose build
$ docker-compose up
```

## container
```
$ docker exec -it docker_cakephp2_web_1 /bin/bash
$ docker exec -it docker_cakephp2_db_1 /bin/bash

$ chmod 755 docker.sh
$ ./docker.sh web
$ ./docker.sh db
```
