# Docker Cmds

# Index

## Installation:

```powershell
apt install docker.io
```

## Basic_CMD:

- List all the Images:
    
    ```
    docker images
    docker images -a
    ```
    
- Remove the image:
    
    ```
    docker rmi <IMAGE ID>
    
    OR
    
    docker rmi -f <IMAGE ID>
    ```
    
- Download Image:
    
    ```
    docker pull <IMAGE NAME>
    ```
    
- Run The image
    
    ```
    docker run <IMAGE ID>
    ```
    
    ## Build_Docker_Image:
    
- Make ==Dockerfile== a text file containig all the cmds:
- Run cmd to make docker
    
    ```powershell
    docker image build **PATH_OF_THE_Dockerfile_1DIRECTORY**
    ```
    
    OR
    
    ```powershell
    docker image build -t : <**DIRECTORY OF DockerFile** > ```
    ```
    

## Get Docker Shell:

```powershell
docker run -it --name=<image_name> <name>:<tag> bash

docker build . //if Dockerfile is in the current working directory
```

## List Docker containers processes and COMMANDS:

- run:
    
    ```kotlin
    docker container ps
    ```
    
- Remove the container process:
    
    ```kotlin
    docker container rm -f <process_id>
    
    // to remove by name
    
    docker container rm /es-node01
    ```
    
- STOP container:
    
    ```kotlin
    docker container stop <container>
    ```
    

## LIST network in docker:

- list networks:
    
    ```kotlin
    docker network ls
    ```
    
- remove network:
    
    ```kotlin
    docker network rm <ID_network>
    ```
