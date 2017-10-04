# docker-mysql [![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](LICENSE) [![Docker Automated buil](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/u/id2s/docker-mysql/)

Docker image for MySQL 5.1.73 database based on official [MySQL](https://hub.docker.com/_/mysql/) image

## Installation

- [Install Docker](https://docs.docker.com/engine/installation/)
- Run docker commnad to get an image: `docker pull id2s/docker-mysql:5.1`
- Validate image successfully downloaded: `docker images`

## Run 

Start a **mysql** server instance:
    
    # General form
    $ $ docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]
    
    # Example
    $ docker run -d --name mysql-5.1 -p 3307:3306 -e MYSQL_ROOT_PASSWORD=[password] id2s/docker-mysql:5.1

Other **commands**:

    # Kill the container
    docker kill [container-id]
    
    # Shell script/shell access
    $ docker exec -it mysql-5.1 bash
    
    # Viewing MySQL logs
    $ docker logs mysql-5.1
    
    # Start exisitng container (often: after Docker Engine update)
    docker start [CONTAINER ID]