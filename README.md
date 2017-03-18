# Docker ahoi! - Round 1

## Goals

* Write your own Dockerfile
* Learn basic Docker Commands

## Help

* [Docs](https://docs.docker.com)
* [Docs > Dockerfile](https://docs.docker.com/engine/reference/builder/)
* [Docs > Commandline](https://docs.docker.com/engine/reference/commandline/cli)

## Tasks - Round 1

### Write your first Dockerfile

✓ Fill out `Dockerfile`

### Build docker image

    docker build -t docker-ahoi:round-1 .

### Run docker container

    docker run docker-ahoi:round-1 -p 5000:5000 --name=ahoi-r1

To publish all ports of container 1:1

    docker run docker-ahoi:round-1 -P --name=ahoi-r1

### List running docker containers

    docker ps
    # alt: docker container ls

### Stop docker container

    docker stop ahoi-r1
    # docker kill ahoi-r1 # hard kill

### List all docker containers

    docker ps -a

### Remove created container

    docker rm ahoi-r1

### Run docker container with removal

    docker run docker-ahoi:round-1 -p 5000:5000 --name=ahoi-r1 --rm 

### Run docker container in background

    docker run docker-ahoi:round-1 -p 5000:5000 --name=ahoi-r1 -d

### Step into container

    docker exec ahoi-r1 -it sh
    docker exec ahoi-r1 -it sh --tty

### Stop container

    docker stop ahoi-r1

### Start container

    docker start ahoi-r1

### Run docker container and step into

    docker run docker-ahoi:round-1 -p 5000:5000 --name=ahoi-r1 -rm -it sh

### Run docker container with mounted volume

    docker run docker-ahoi:round-1 -
