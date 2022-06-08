# notes

## docker 
time : 22-06-08
author : tomcao(TC)

1. **sudo usermod -aG docker $USER** 

> This command is to prevent you type sudo in front of docker everytime

2. **docker run -it ubuntu:latest**

> The -i flag tells docker to keep STDIN open to your container, and the -t flag allocates a pseudo TTY for you. Basically you need both for you to have a shell into your newly started container. Try installing some packages from apt or just play around. It should look like a bare Linux system.

3. **docker build -t missile:latest .**

> This tells Docker to look in the current directory for a Dockerfile to build, and builds it. The -t flag tells Docker to tag this build with the name missile:latest. Note that building the missile image will take a couple of minutes to complete.


docker search             Search Docker Hub for pre-built images

docker pull               Pull an image or a repository from a registry

docker images             List images

docker build              Build an image from a Dockerfile

docker run                Run a command in a new container

docker ps                 List containers

docker start/stop/restart Start/stop/restart a container

docker exec               Run a command in a running container

docker inspect            Return low-level information on Docker objects

docker rm                 Remove one or more containers

docker rmi                Remove one or more images

4. **docker run -d httpd**

> 9b02644747a8   httpd     "httpd-foreground"   4 minutes ago   Up 4 minutes   80/tcp    clever_chaplygin

5. 
> docker run -d -p 4000:80 httpd
> docker run -d -p 4001:80 httpd
> docker run -d -p 4002:80 httpd

> cc101f08c931   httpd     "httpd-foreground"   3 seconds ago    Up 3 seconds    0.0.0.0:4002->80/tcp, :::4002->80/tcp   dreamy_shamir
> 1369916fb19d   httpd     "httpd-foreground"   11 seconds ago   Up 10 seconds   0.0.0.0:4001->80/tcp, :::4001->80/tcp   hopeful_mahavira
> c4a6cfeab90e   httpd     "httpd-foreground"   15 seconds ago   Up 15 seconds   0.0.0.0:4000->80/tcp, :::4000->80/tcp   gracious_colden
> 9b02644747a8   httpd     "httpd-foreground"   5 minutes ago    Up 5 minutes    80/tcp                                  clever_chaplygin

