# Docker Cheat-sheet

## Docker 
docker version --- shows version of Docker Engine(Client and Server)  

## Docker system [Command]
docker system df --- shows docker's disk usage  
docker system info --- display system-wide information  
docker system events --- shows realtime events from a server  
docker system prune --- remove unused data  

## Docker image  [Command]
docker pull [image] --- download an image  
docker image ls --- shows list of images  
docker images --- shows list of images  
docker image build -t test:latest . --- build an image from Dockerfile
docker image rm [image] --- remove an image  
docker image rm $(docker image ls -q) -f --- remove all images  

## Docker container  [Command]
docker container ls --- shows all running containers  
docker container ls -a --- shows all containers(even stopped)  
docker container run -it ubuntu:latest bin/bash --- run ubuntu container and open bash  
docker container run -d --name web1 --publish 8000:8080 test:latest  --- run test image as a daemon and bind ports
docker container run -it microsoft/powershell:nanoserver pwsh.exe --- run windows nanoserver and open Powershell  
docker container exec [options] [container-name or container-id] [command/app] --- atach to the running container  
docker container exec -it [container-name] pwsh.exe --- attach to the running windows container  
docker container exec -it [container-name] bash --- attach to the running linux container  
docker container start [OPTIONS] CONTAINER [CONTAINER...] --- start a container  
docker container stats [OPTIONS] [CONTAINER...] --- displays a live stream container's resource usage stats  
docker container stop [OPTIONS] CONTAINER [CONTAINER...] --- stop a container  
docker container rm [OPTIONS] CONTAINER [CONTAINER...] --- remove a container  
docker container prune [OPTIONS] --- remove all stopped containers  
docker container rm $(docker container ls -aq) -f --- remove all containers  

## Docker Compose [Command]
docker-compose up --- start services  
docker-compose up & --- start services with debug information  
docker-compose up -d --- start services as daemons  
docker-compose down --- stop services and delete container  
docker-compose stop --- stop services  
docker-compose restart --- restart services  
docker-compose ps --- show information about services  
docker-compose top --- the command that shows processes running inside of each service  

## Useful links
https://labs.play-with-docker.com/ --- the way of spinning up temporary Docker environment  

## Shortcuts
Ctrl+PQ --- leave container without terminating it