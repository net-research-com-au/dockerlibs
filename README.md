# dockerlibs
List of Docker images and how tos for IT Infrastrcure admins 

## Docker image list

|Docker Name|Description|Purpose|Link|
|-|-|-|-|
|jupyter/datascience-notebook| DockerHub image. includes libraries for data analysis from the Julia, Python, and R communities.|Datat science and Data analysis using jupyter notebooks|https://hub.docker.com/r/jupyter/datascience-notebook|
|mcr.microsoft.com/azure-cli:latest| DockerHub image. Running azure cli| Manage Azure using Azure cli| https://github.com/microsoft/containerregistry|
|cytopia/ansible:latest-azure|DockerHub image. Ansible with Azure cli tools | For infrastructure CI/CD |https://github.com/cytopia/docker-ansible|

## docker commands
```shell
sudo docker ps -a       # list of all docker containers in the system
sudo docker ps -a -q    # list of all docker containers ids only
sudo docker start <continer id>    # start a container
sudo docker stop <continer id>    # stop a container
sudo docker attach <continer id>    # attach to console of container
sudo docker rm <continer id>    # remove container instance (NOTE: does not delete the container base image)
sudo docker rm $(sudo docker ps -a -q -f status=exited)  # remove docker instances which are exited or stoped
sudo docker prune # this will also remove all stoped docker instances
sudo docker rmi <image name>  # deletes the image from the local system
```

## docker build for python
Python Docker build for python development

```shell
cd kitpython-docker
docker build -t kitpython:v1 .
docker run -it kitpython:v1
```

Push to docker repo
```shell
docker login
docker tag kitpython:v1 dbnetdocker/kitpython:v1
docker push dbnetdocker/kitpython:v1
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



