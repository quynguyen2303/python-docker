# Welcome to Docker Python

This is a repo for new users getting started with Docker and Python.

You can try it out using the following command.

Active the enviorment
```
source python_docker/bin/activate
```

Run the docker image 

```
docker run python-docker
```

Publish a port of a container to outside port (host)

```
[host port]:[container port]
docker run --publish 8000:5000 python-docker
```

Run server in detached mode ```--detach``` or ```-d```

```
docker run -d -p 8000:5000 python-docker
```

Name a container

```
docker run -d -p 8000:5000 --name rest-server python-docker
```

And open `http://localhost:8088` in your browser.

# Container

List all running containers

``` 
docker ps
docker ps --all
```

Stop/Restart a container

```
docker stop [container_name]
docker restart [container_name]
```

Remove a container

```
docker rm [container_name]
```

# Building

Maintainers should see [MAINTAINERS.md](MAINTAINERS.md).

Build and run:
```
docker build -t welcome-to-docker . 
docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
```
Open `http://localhost:8088` in your browser.