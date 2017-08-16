
[![][ElasTest Logo]][ElasTest]

Copyright © 2017-2019 [ElasTest]. Licensed under [Apache 2.0 License].

elastest/docker-compose-siblings 
==============================

## What is this? 

This image is a extension of the basic environment (docker-siblings) that add: docker-compose, npm, node and angular.

## Supported tags and respective `Dockerfile` links
-	[ `latest` (*1.0/Dockerfile*)](https://github.com/elastest/ci-images/commits/master/docker-compose-siblings/Dockerfile)

## Quick reference

-	**Where to get help**:  
	[the ElastTest mailing list](), [the Elastest Slack](), or [Stack Overflow]()

-	**Where to file issues**:  
	[--]()

-	**Maintained by**:  
	[the ElasTest community](https://github.com/elastest)

-	**Published image artifact details**:  
	[repo-info repo's `elastest/ci-images` directory](https://github.com/elastest/ci-images/blob/master/<image-name>) ([history](https://github.com/elastest/ci-images/commits/master/<image-name>))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images PRs with label `elastest/ci-images`](https://github.com/elastest/ci-images/pulls?q=label%3Alibrary%2Fmysql)  

-	**Source of this description**:  
	[docs repo's `ci-docker-compose-siblings/` directory](https://github.com/elastest/ci-images/tree/master/docker-compose-siblings) ([history](https://github.com/elastest/ci-images/commits/master/docker-compose-siblings))

-	**Supported Docker versions**:  
	[the latest release](https://github.com/docker/docker/releases/latest) (down to 17.03.1 on a best-effort basis)

# What's on this image?

This image provides an environment with the following tools installed:
- Oracle Java 8
- Apache Maven 3.3.9
- docker-ce (latest stable)
- AWS cli 
- Docker-compose
- npm
- Node
- Angular CLI


# How to use this image

This image should be launched while linked with the docker-host as follows:

- Docker run (without aws): 
```
docker run -u jenkins -v /var/run/docker.sock:/var/run/docker.sock:rw elastest/ci-docker-compose-siblings 
```

- Docker run (with aws): 
```
docker run -u jenkins -v /var/run/docker.sock:/var/run/docker.sock:rw -v <aws config files path>:/home/jenkins/.aws elastest/ci-docker-compose-siblings 
```

- Jenkins pipeline: 
```
def mycontainer = docker.image('elastest/ci-docker-compose-siblings:latest')
mycontainer.pull() 
mycontainer.inside("-u jenkins -v /var/run/docker.sock:/var/run/docker.sock:rw -v <aws config files path>:/home/jenkins/.aws") { //here your code }
```

## Dependencies (other containers or tools)

This container needs the following to work properly:

- docker installed in the host with the posibility to be shared. 

- aws configuration, you can avoid running the container with the aws volume if you don't use the aws cli. For information of the configuration files please visit the [Amazon Reference on Config Files](http://docs.aws.amazon.com/cli/latest/userguide/cli-config-files.html) 



[Apache 2.0 License]: http://www.apache.org/licenses/LICENSE-2.0
[ElasTest]: http://elastest.io/
[ElasTest Logo]: http://elastest.io/images/logos_elastest/elastest-logo-gray-small.png
[ElasTest Twitter]: https://twitter.com/elastestio
[GitHub ElasTest Group]: https://github.com/elastest
