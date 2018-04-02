# cakephp2

## docker for mac
https://docs.docker.com/docker-for-mac/install/

## setup
```
$ git clone https://github.com/basi/cakephp2
$ cd cakephp2/www/
$ git clone -b 2.x git://github.com/cakephp/cakephp.git
$ cd ../
$ docker-compose build
$ docker-compose up
```

## container
```
$ docker exec -it cakephp2_web_1 /bin/bash
```
