# AWS CodeBuild

Ubuntu 18 docker image for AWS CodeBuild. Containing nodejs 10 and postgres 11.

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

# Get prebuild image from docker hub
```
$ docker pull ivacko/aws-codebuild
```

# Run image on CodeBuild
The image have to be run with privileged mode enabled when used on CodeBuild.