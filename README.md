# AWS CodeBuild

Ubuntu 14.04.5 docker image for AWS CodeBuild. Containing nodejs 8.11 and postgres 10.

# Image build steps
```
$ git clone https://github.com/Ivacko/aws-codebuild-docker-nodejs-postgres
$ cd aws-codebuild-docker-nodejs-postgres
$ cd bin
$ docker build -t aws-codebuild:v1 .
```
Run postgres manually:
```
$ docker run -it aws-codebuild:v1 bash
$ service postgresql start
```

Run image as postgres server:
```
$ docker run -p 5432:5432 --name postgres aws-codebuild:v1
```

Get pre-build image from docker hub
```
$ docker pull ivacko/aws-codebuild-postgres
```