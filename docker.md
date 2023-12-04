# Top commands

# Other commands
## Show all nerworks
docker network ls


# Image
## Current images
docker images
## Download new images
docker pull ubuntu bash
## run docker image
docker run -it ubuntu
## remove image
docker image rm bbd5a0640322
## run docker image and mount a disc (current project)
### powershell
docker run -v C:\Users\ilyao\Docker_projects\docker_jupyterlab\:/home/jovyan -p 8888:8888 quay.io/jupyter/scipy-notebook:latest
### WSL
docker run -v /mnt/c/Users/ilyao/Docker_projects/docker_jupyterlab/:/home/jovyan/ -e JUPYTER_ALLOW_INSECURE_WRITES=1 -p 8888:8888 quay.io/jupyter/scipy-notebook:latest


# Build and docker-compose
## Run our docker-compose instruction
docker-compose up
## Build an image from a Dockerfile
docker build -t flask_app .
## run our docker build 
docker run -d -p 5001:5000 flask_app
## create our 
docker-compose build --no-cache && docker-compose up -d
##
docker-compose up -d

# Container
## Current containers
docker ps -a
## Restart already closed container
docker container restart 89360080057f
## Stop one or more running containers
docker stop 383096e6a767
## Remove containers
docker rm 383096e6a767
## go into our container
docker exec -it 89360080057f bash
## daemon start
docker run -d flask_app


docker-compose exec airflow airflow db init

# reload our docker-compose
docker-compose down
## Detached mode: Run containers in the background
docker-compose up -d


```python
from cryptography.fernet import Fernet
fernet_key= Fernet.generate_key()
print(fernet_key.decode())
```