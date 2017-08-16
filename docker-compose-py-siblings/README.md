[![][ElasTest Logo]][ElasTest]

Copyright © 2017-2019 [ElasTest]. Licensed under [Apache 2.0 License].

elastest-docker-compose-py-siblings
==============================

# ElasTest Docker Build Image with Python Support

===============================

# Supported tags and respective `Dockerfile` links
-	[`latest`](https://github.com/elastest/ci-images/docker-compose-py-siblings/Dockerfile)

# Quick reference

-	**Where to get help**:  
	[the ElastTest mailing list](), [the Elastest Slack](), or [Stack Overflow]()

-	**Where to file issues**:  
	[--]()

-	**Maintained by**:  
	[the ElasTest community](https://github.com/elastest)

-	**Published image artifact details**:  
	[repo-info repo's `elastest/environments` directory](https://github.com/elastest/ci-images/blob/master/<image-name>) ([history](https://github.com/elastest/environments/commits/master/<image-name>))  
	(image metadata, transfer size, etc)

<!--
-	**Image updates**:  
	[official-images PRs with label `elastest/ci-<image-name>`](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Fmysql)  

-	**Source of this description**:  
	[docs repo's `mysql/` directory](https://github.com/docker-library/docs/tree/master/mysql) ([history](https://github.com/docker-library/docs/commits/master/mysql))
-->

-	**Supported Docker versions**:  
	[the latest release](https://github.com/docker/docker/releases/latest) (down to 17.03.1 on a best-effort basis)

# What's on this image?
This image has all the packages installed by `elastest/docker-compose-siblings` and python 3.6 along with testing tools of:

 * flask_testing
 * coverage
 * nose
 * pluggy
 * py
 * randomize
 * tox

# How to use this image

The intended use of this image is within a `Jenkinsfile`.

To build it from the `cwd`:

`docker build -t elastest/ci-docker-compose-py-siblings:latest ./`

## Dependencies (other containers or tools)

None

## Integration with other containers or tools)

None

[Apache 2.0 License]: http://www.apache.org/licenses/LICENSE-2.0
[ElasTest]: http://elastest.io/
[ElasTest Logo]: http://elastest.io/images/logos_elastest/elastest-logo-gray-small.png
[ElasTest Twitter]: https://twitter.com/elastestio
[GitHub ElasTest Group]: https://github.com/elastest