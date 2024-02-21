# Docker Notes
## Problem Statement
- Setting up of the same environment on every different machine where we wanted the application to run properly was a time taking and repetative task.

## Solution
- Using containers , in these containers we setup our config , then we can share these container with other people and these containers are system independent which means these containers can run in any system.
- Hence there is no need of setting up the same environment again and again.
- These containers are very light weight , are easy to create and destroy.
- Each container has it's own Operating System (OS), tools and configiration.

## Docker Daemon
- It's a tool that actually does the work,creating images ,pulling images,spin ups the containers, scale down the containers, create the containers.

## Docker Desktop
- It's a GUI , which displays the machine state.

## Docker Hub
- Github for containers, where all the public containers are present and we can pull the containers to use them locally.

## Images
- Images are like OS and to run these images we need Containers.
- A single image can run in multiple containers, and each container will be independent or isolated from other containers.
- Like 2 different laptops running the same windows, but both the laptops will have some data which is isolated from the other laptop, similarly the same case is with containers.
- We can share data between these multiple containers if we want to , and by default these containers are isolated.
- When in development, we create our custom image which has some configuration.
- These custom images can be deployed on any cloud platform like Amazon etc, using containers.

## Container
- Containers are just machines.
- These containers are isolated from the outer machine, and anything done inside these containers won't affect the parent machine.



## -------------🧑‍💻🧑‍💻 Commands 🧑‍💻🧑‍💻-------------

1. - To create and run an image : docker run -it (imageName)
   - ex : docker run -it ubuntu
   - `-it` stands for interactive tty mode, this tells that run the command and connect my main device terminal to the container terminal and don't disconnect it.

2. To list all the running docker containers : docker container ls
3. To list all the docker containers : docker container ls -a
4. To start a container : docker start (containerName)
5. To stop a running container : docker stop (containerName)
6. - To execute/run a command in a container : docker exec (containerName) (command)
    - ex : docker exec random-name ls

7. - To open the terminal for that container and not disconnect from it : docker exec -it (containerName) bash
    - we can't open the terminal for a container without the -it flag.

8. To list all the images: docker images
