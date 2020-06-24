# verify-aws-quotas-CDP-PC

---

---

## Notes:
*  This was built and tested on Docker Version 19.03.8
*  This assumes you already have Docker installed.
*  All steps below are run from a terminal/ssh window

---

### Install Docker onto your computer --> [Install Steps](https://docs.docker.com/engine/install/)

### Docker Container Setup Steps:

---

```
# Pull docker image centos 7
docker pull centos:7

# Create a docker volume to persist data
docker volume create verify-aws-quota-vol1

# inspect volume
docker volume inspect verify-aws-quota-vol1

# list volumes
docker volume ls



# run a new docker container with this volume from centos image

 docker run -it \
  --name centos_verify_aws_quota \
  --mount source=verify-aws-quota-vol1,target=/app \
  centos:7 bash

```

---

### Pull git repo into this new container to setup CDP Pre-Reqs

```
# install git 
yum install -y git
cd /app
git clone https://github.com/tlepple/verify-aws-quotas-CDP-PC.git
cd /app/verify-aws-quotas-CDP-PC
```

---

| Provider         | Readme Document  |
| ---------------- | ---------------- |
| AWS              | [Setup Steps](https://github.com/tlepple/verify-aws-quotas-CDP-PC/blob/master/documentation/aws_user.md)|
| AWS              | [Terminate Steps](./terminate_readme.md)|

---
---

# Usefull docker command reference:

---

```
# list all containers on host
---------------------------------------------
docker ps -a

#  start an existing container
---------------------------------------------
docker start centos_verify_aws_quota

# connect to command line of this container
---------------------------------------------
docker exec -it centos_verify_aws_quota bash

#list running container
---------------------------------------------
docker container ls -all

# stop a running container
---------------------------------------------
docker container stop centos_verify_aws_quota

# remove a docker container
---------------------------------------------
docker container rm centos_verify_aws_quota

# list docker volumes
---------------------------------------------
docker volume ls

# remove a docker volume
---------------------------------------------
docker volume rm verify-aws-quota-vol1


```
