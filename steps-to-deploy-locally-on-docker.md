# Steps to deploy on Docker locally

## https://hub.docker.com/_/ubuntu


## Install docker

```sh
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
docker --version
```

## Download image

```sh
docker pull ubuntu
```

## Create and start docker container interactive and detach with code mapping for ubuntu image

```sh
docker run -dit -p 8080:8080 ubuntu /bin/bash
```

## List all containers

```sh
docker ps -a
```

## Go into docker container

```sh
docker exec -it <container_id> /bin/bash
# Or
docker exec -it <container_name> /bin/bash
```

## Update container

```sh
sudo apt-get update -y && sudo apt-get upgrade -y
```

```sh
sudo apt-get install curl unzip -y
```

## Install AWS CLI

```sh
curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip"
unzip -u awscliv2.zip
./aws/install --bin-dir /usr/local/bin --install-dir /usr/local/aws-cli --update
which aws
ls -l /usr/local/bin/aws
```

```sh
aws --version
```

# Choose your region and country when prompt
## Configure AWS Configuration

```sh
aws configure
```

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=/9fmfoI3U
AWS_DEFAULT_REGION=us-east-1

## Since model upload after training and application will download model from s3, hence we need to configure

```sh
AWS_ACCESS_KEY_ID=<your-access-key>
AWS_SECRET_ACCESS_KEY=<your-secret-access-key>
AWS_DEFAULT_REGION=us-east-1
```

```sh
export MONGODB_URL="mongodb+srv://howcool:z4E32JwhsC12LQTK@cluster0.oa9kol7.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0"
```

```sh
export AWS_ACCESS_KEY_ID=""
export AWS_SECRET_ACCESS_KEY=""
export AWS_DEFAULT_REGION="us-east-1"
```

## Install python

```sh
sudo apt-get install python3-full -y
```

## install pip      
```sh
apt-get install pip -y
```

```sh
apt-get install mesa-utils -y
```

## install git nano vim
```sh
apt-get install git -y
apt-get install nano -y
apt-get install vim -y
```

## Clone Repository

```sh
git clone https://github.com/python-devops-sre/US-Visa-Approval-Prediction.git
```

## Change directory to clonned repository

```sh
cd US-Visa-Approval-Prediction
```

```sh
python3 -m venv path/to/venv
source path/to/venv/bin/activate
```

## Install all requirement - Note: you may need to comment line with notebook

```sh
pip install -r requirements.txt
```

## Check if AWS CLI is 

```sh
aws --version
```

## exist from docker and then go into docker container

```sh
docker ps -a
docker exec -it <container_id> /bin/bash
```
docker exec -it 46faaa72e730 /bin/bash

## execute application

```sh
python3 app.py
```

## List all containers

```sh
docker ps -a
```

## Go into docker container - Skip this step
```sh
docker exec -it <container_id> /bin/bash
```

### Exit Docker Container without Stopping It
- If you want to exit the container's interactive shell session, but do not want to interrupt the processes running in it, press Ctrl+P followed by Ctrl+Q. This operation detaches the container and allows you to return to your system's shell

```sh
docker commit <container_id>
```
docker commit 46faaa72e730 howcool/end-to-end-usvisa-prediction-mlmodel

```sh
docker image tag <image_id> <dockerhubid>/<name on dockerhub>:latest
```
docker image tag 8a5162116265 howcool/end-to-end-object-detection:latest

```sh
docker push <image id>
```
docker push howcool/end-to-end-usvisa-prediction-mlmodel 

#### Commands to pull image from docker hub and run it locally

```sh
docker pull howcool/end-to-end-usvisa-prediction-mlmodel:latest
```

```sh
docker run -dit -p 8080:8080 howcool/end-to-end-usvisa-prediction-mlmodel /bin/bash
```

## List all containers

```sh
docker ps -a
```

## Go into docker container

```sh
docker exec -it <container_id> /bin/bash
```

```sh
cd End-to-end-Object-Detection-Project/
source path/to/venv/bin/activate
python3 app.py
```

# Docker image

https://docs.docker.com/engine/reference/commandline/image/#examples


## List all images

```sh
docker image ls
```

# Docker command line interface (CLI)

```sh
https://docs.docker.com/engine/reference/commandline/

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=
```

## Stop all running container (reference only)

```sh
docker stop $(docker ps -a -q)
```

## Remove all stopped container (reference only)

```sh
docker rm $(docker ps -a -q)
```

## Remove all images

```sh
docker rmi $(docker images -a -q)
```

## to list all containers (reference only)
```sh
docker ps -a
```

## to list all images (reference only)
```sh
docker image ls
```

# docker-compose

https://docs.docker.com/compose/


# dockerfile

```sh
https://docs.docker.com/engine/reference/builder/#run
```
```sh
docker ps -a
```
```sh
docker restart <container_id>  #8f1a99a79b3d
```
```sh
docker exec -it <container_id> /bin/bash
# docker exec -it 8f1a99a79b3d /bin/bash
```
```sh 
source path/to/venv/bin/activate
```
```sh 
python3 app.py
```
