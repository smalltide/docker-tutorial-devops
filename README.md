# docker-tutorial-devops
Learn Docker and Devops from Udemy course. Docker Technologies for DevOps and Developers

Docker Technologies for DevOps and Developers  
https://www.udemy.com/docker-tutorial-for-devops-run-docker-containers

1. Docker
2. DevOps
3. Docker Compose
4. Docker Swarm
5. Docker Machine
6. DockerHub
7. CirclCI
8. DigitalOcean

Show docker images list
```
  > docker images
```
Login DockerHub
```
  > docker login
```
docker run
```
  > docker run busybox:1.24 echo "hello world"
  > docker run busybox:1.24 ls /
  > docker run -it busybox:1.24 (interactive mode)
  > docker run -d busybox:1.24 sleep 1000 (docker run in background mode)
  > docker run --rm busybox:1.24 sleep 1 (remove when finish run)
  > docker run --name hello_world busybox:1.24 (define name for container)
```
docker inspect
```
  > docker inspect <container id>
```
docker inspect
```
  > docker inspect <container id>
```
docker logs
```
  > docker run -it -d -p 8888:8080 tomcat:8.0 (-p host_port : container_port)
  > docker logs <container id>
```
docker image layer history
```
  > docker history busybox:1.24
  >
  > docker run -it debian:jessie
  > apt-get update && apt-get install -y git (install git in container)
  > exit
  > docker history debian:jessie
```
docker commit to create image
```
  > docker container ls -a
  > docker commit <container id> smalltides/debian:1.0 (commit a new image from container id)
  > docker images
  > docker history smalltides/debian:1.0
  > docker run -it smalltides/debian:1.0
```
Docker file to create image
```
  > docker build -t smalltides/debian .
  > docker images
  > docker history smalltides/debian:latest
  > docker build -t smalltides/debian:latest . --no-cache=true (no cache mode)
```
push docker image to docker hub
```
  > docker login (must login docker hub)
  > docker tag <image id> smalltides/debian:1.01
  > docker push smalltides/debian:1.01
```
use Dcokerfile to create a containerize python app
```
  > docker build -t dockerapp:0.1 .
  > docker run -d -p 5000:5000 <image id>
  > docker exec -it <container id> bash
  > ps aux
```
