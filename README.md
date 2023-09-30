# Watchtower

A container-based solution for automating Docker container base image updates.

<br />

## Installation 

1. Download folder.

2. Create the file ./.docker/.env using ./.docker/.env.example as template.

3. Go inside folder `./docker` and run `docker-compose up -d --build` to start containers.

<br />

## Exclude containers from watchtower

If you need to exclude some containers, set the com.centurylinklabs.watchtower.enable label to false. For clarity this should be set on the container(s) you wish to be ignored, this is not set on watchtower.

```yml
version: "3"
services:
  someimage:
    container_name: someimage
    labels:
      - "com.centurylinklabs.watchtower.enable=false"
```