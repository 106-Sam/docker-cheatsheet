# Docker-Notes

**Docker** - Docker is containerisation tool, provides packaging the application and bundles all dependencies.

- using docker we can create containers.

- A docker container image is a lightweight, and executable package. It includes everything needed to run an application like code, runtime(java), system tools, system libraries and settings.

- Docker is a tool designed to  make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package And importantly, **Docker is open source**.


#### Docker Commands

- `docker -v` (version)
- `service docker start` (or) `systemctl start docker` - (To start the docker service).
- `docker image`  - to check any installed images.
- `docker pull <image_name>` - to install operating system.
- `docker run - it <image name or id>`  - (it means interactive shell) to create a container and enter into it.
- `docker ps -a`  - shows running or exited containers.
- `docker run -it --name <unqiue_name> <imagename or id> ` - to create a container using a name.

*Note*: press ctrl + p + q (to get out of docker without stopping the container)

- `docker info`  - shows docker containers information.
- `docker ps` - shows only running containers.
- `docker start <container_id or cont_name>` - to start the exited containers.
- `docker stop <container_id or cont_name>` - to stop a container.
- `docker pause <container_id or cont_name>` - we can pause only the running containers. You cannot or start this container.
- `docker unpause <container_id or cont_name>` - we can unpause the paused container
- `docker attach <container_id or cont_name>` - to enter into a running container.
- `docker exec  -it <container_id or cont_name> /bin/bash`  - another way to enter into the running container. When we type the exit it does come out of the container but doesn't stop the container.


---

![VMs vs Containers](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/bltb6200bc085503718/5e1f209a63d1b6503160c6d5/containers-vs-virtual-machines.jpg)



**Namespaces** are one of the feature in the Linux Kernel and fundamental aspect of containers on Linux. On the other hand, namespaces provide a layer of isolation. Docker uses namespaces of various kinds to provide the isolation that containers need in order to remain portable and refrain from affecting the remainder of the host system. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.

Source: [Docker namespace and Control groups](https://medium.com/@kasunmaduraeng/docker-namespace-and-cgroups-dece27c209c7)

- `docker rm -f <cont_id or cont_name>` - to delete a container.
- `docker rmi <img_id or repo_name>` - to delete an image. (multiple images can be removed at once)

*Note*: all images come from [docker's hub](https://hub.docker.com/) , just like GitHub repositories. We can search for images on docker hub.

- `docker search <image_name>` - to search for a particular image (eg. kali)
- `docker commit <cont_id or cont_name)>` - to create image of a customised container.
- `docker tag <img_id> <customized_name>` - to give repository name(small letters only) by default it takes tag as latest.
- `docker tag <img_id> <customized_name>:v1` - same as above but now tag name is changed to v1.
***
