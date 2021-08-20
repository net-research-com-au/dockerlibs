# dockerlibs
List of Docker images and how tos for IT Infrastrcure admins 

## Docker image list
|-|-|-|-|
|Docker Name|Description|Purpose|Link|
|-|-|-|-|
|jupyter/datascience-notebook| DockerHub image. includes libraries for data analysis from the Julia, Python, and R communities.|Datat science and Data analysis using jupyter notebooks|https://hub.docker.com/r/jupyter/datascience-notebook|
|jupyter/datascience-notebook:latest| DockerHub image. Running azure cli| Manage Azure using Azure cli| https://github.com/microsoft/containerregistry|
|-|-|-|-|

## docker commands
```shell
sudo docker ps -a       # list of all docker containers in the system
sudo docker ps -a -q    # list of all docker containers ids only
sudo docker start <continer id>    # start a container
sudo docker stop <continer id>    # stop a container
sudo docker attach <continer id>    # attach to console of container
sudo docker rm <continer id>    # remove container instance (NOTE: does not delete the container base image)
```

# How to use
## jupyter/datascience-notebook

run below command to start a docker
- maps your local windows directory C:\Mystuff\datascience --to--> /home/jovyan/work with in docker container
- starts interactive bash shell
- exposes port 8888
```shell 
# windows example
docker run -it -p 8888:8888  -v C:\Mystuff\datascience:/home/jovyan/work jupyter/datascience-notebook 

# linux example
docker run -t -p 8888:8888 -v ~/scripts/datascience:/home/jovyan/work jupyter/datascience-notebook
```



