
# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t horiring/nginx .
  docker build --rm -t horiring/docker_build:0.6 ./
  mkdir ~/df
  docker run -it --name cc1 -v ~/df:/var/www/html -p 80:80 horiring/nginx
	docker run -it --name c1 -v ~/df:/var/www/html -p 80:80 horiring/nginx
  docker run -it --name ejej1 -v ~/df:/var/www/html -p 80:80 horiring/docker_build:0.6
  echo "<h1>hi</h1>" > ~df/index.html
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        nowage/centos7      "/bin/bash"         7 seconds ago       Up 6 seconds                            c1
```

To test, ("nowage" is username. )
```
echo "<h1>hi</h1>" > ~df/index.html
	127.0.0.1
```
To Rollback
```
    docker rm c1 -f
    docker rmi nowage/centos7
```
