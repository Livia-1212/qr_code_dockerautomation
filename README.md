# Devops Demo 
**Screenshots**

1. Put the screenshot of your image in your Docker account here.

![image on my Docker account](https://github.com/Livia-1212/qr_code_dockerautomation/blob/main/Images.png)



## Basic Commands (self-made note)
**Container Management** \
'''sh
docker ps\
'''
 list all running containers

>docker run \
 create and start a new container from an image. eg. docker run -d -p 8080:80 httpd

>docker run -e [key]=[value] \
 This command sets an environment variable inside the Docker container.

>docker run -d \
 This runs the container in detached mode (in the background).

>docker run -p [host_port]:[container_port] \
 This command maps a port on your local machine (host) to a port inside the Docker container.

> docker run -v [host_directory]:[container_directory] \
 This command bind mounts a volume from your host machine to your container.. refers to the current directory on your host machine (where you are running the command from).
 /app/something is the directory inside the Docker container where you want to mount your local directory.
 This means that any changes you make in the host directory (.) will be reflected in the container directory (/app/something), and vice versa.
 It's often used to persist data (like logs or app files) or to allow the container to access files from the host machine.

>docker run --env-file [file_name] \
 This allows you to load environment variables from a file into the container.

>docker stop [containername_or_id] \
 stop a running container

> docker exec -it [containername_or_id] bash \
 start a new shell session inside a running container (use bash or sh depending on the container)

> docker rm [containername_or_id]\
 remove a container(must stop it first)

**Image Management** \
> docker images \
 list all available images on your local machine

>docker pull [image_name] \
 download an image from Docker Hub or a registry

> docker build -t [image_name] [path_to_dockerfile] \
 build a Docker image from a Dockerfile

> docker tag [image_name_or_id] [new_image_name] \
 Tag an image with a new name or version

> docker commit OPTIONS 'messages' CONTAINER [new_image_name] \
 OPTIONS: -a:Author Name of the image, -m:Commit message describing the changes
 --change: Apply Dockerfile instructions to the committed image
 CONTAINER: The name or ID of the container you want to create an image from.
 new_image_name: The name of the new image you want to create.
 The docker commit command is used to create a new image from an existing container. When you run this command, Docker saves the current state of a container as a new image, allowing you to reuse that state in future containers.


 
