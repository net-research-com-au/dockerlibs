# dockerlibs
List of Docker images and how tos for IT Infrastrcure admins 

## Docker image list
|-|-|-|-|
|Docker Name|Description|Purpose|Link|
|-|-|-|-|
|jupyter/datascience-notebook| DockerHub image. includes libraries for data analysis from the Julia, Python, and R communities.|Datat science and Data analysis using jupyter notebooks|https://hub.docker.com/r/jupyter/datascience-notebook|
|-|-|-|-|

# How to use
## jupyter/datascience-notebook

run below command to start a docker
- maps your local windows directory C:\Mystuff\datascience --to--> /home/jovyan/work with in docker container
- starts interactive bash shell
- exposes port 8888
```shell 
docker run -it -p 8888:8888  -v C:\Mystuff\datascience:/home/jovyan/work jupyter/datascience-notebook /bin/bash![image](https://user-images.githubusercontent.com/48237958/130177291-4bb1aac3-776f-432b-baf9-76695511bb59.png)
```



