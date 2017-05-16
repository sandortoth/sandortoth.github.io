![Docker logo](http://sandortoth.github.io/docker-presentation/img/docker_logo.png)

## Docker for Developers - Introduction

###### Sandor Toth
###### Under [Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/) license.
________________________

---

### Topics

#### What is Docker
###### Docker vs VMs
###### Docker History
###### Docker Benefits
###### Common Docker usages
###### Technology behind Docker
###### The Docker architecture

---

### Topics

#### Docker components
###### Docker engine
###### Docker client
###### Docker daemon
###### Docker distribution
###### The docker image
###### The docker container
##### Docker machine / compose / swarm
##### Docker examples / alternatives

---

### Let me ask you

- Who knows about [Docker](http://docker.com)?
- Who uses Docker for development?
- Who uses Docker in production?
- Who tried but could not do it?

---

### What is Docker (v1.13)

> Docker is an open platform for developing, shipping, and running applications.

> Docker allows you to package an application with all of its dependencies into a standardized unit for software development.

---

### Docker vs VMs

![Docker vs traditional Virtualization](https://insights.sei.cmu.edu/assets/content/VM-Diagram.png)

---

### Docker History

 - Solomon Hykes ([@solomonstre](https://twitter.com/solomonstre))
 - dotCloud (now Docker Inc)
 - March 2013
 - Apache 2.0 license
 - 40K+ stars on Github
 - 2000+ contributors
 - 260K+ public repositories on hub.docker.com
 - 240 Meetups in 70 countries
 - 95K Meetup members

---

### Applications are changing

![The challenge](http://sandortoth.github.io/docker-presentation/img/applicationarechanging.png)

---

### The challenge

![The challenge](http://sandortoth.github.io/docker-presentation/img/thechallenge.png)

---

### The matrix from hell
![The matrix from hell](http://sandortoth.github.io/docker-presentation/img/matrixfromhell.png)

---

### Cargo Transport Pre-1960
![The matrix from hell](http://sandortoth.github.io/docker-presentation/img/cargotransport.png)

---

### Also a Matrix from Hell
![The matrix from hell](http://sandortoth.github.io/docker-presentation/img/anothermatrixfromhell.png)

---

### Solution: Intermodal Shipping Container
![The matrix from hell](http://sandortoth.github.io/docker-presentation/img/solutionintermodalcontainer.png)

---

### Docker is a Container System for Code
![The matrix from hell](http://sandortoth.github.io/docker-presentation/img/dockercontainersystemforcode.png)

---

### Docker Eliminates the Matrix from Hell
![The matrix from hell](http://sandortoth.github.io/docker-presentation/img/eliminatematrixfromhell.png)

---

### Why Developers Care

 - Build once... (finally) run anywhere
 - A clean, safe, hygienic, portable runtime environment for your app.
 - No worries about missing dependencies, packages and other pain points during subsequent deployments.
 - Run each app in its own isolated container, so you can run various versions of libraries and other dependencies for each app without worrying.
 - Automate testing, integration, packaging...anything you can script.

---

### Why DevOps Care

 - Configure once... run anything
 - Make the entire lifecycle more efficient, consistent, and repeatable
 - Eliminate inconsistencies between development, test, production, and customer environments.
 - Support segregation of duties.
 - Significantly improves the speed and reliability of continuous deployment and continuous integration systems.
 - Because the containers are so lightweight, address significant performance, costs, deployment, and portability issues normally associated with VMs.

---

### Docker Benefits

 - Fast (deployment, migration, restarts)
 - Secure
 - Lightweight (save disk & CPU)
 - Open Source
 - Portable software
 - Microservices and integrations (APIs)
 - Simplify DevOps
 - Version control capabilities

---

### Common Docker usages

 - Sandbox environment (develop, test, debug, educate)
 - Continuous Integration & Deployment
 - Scaling apps
 - Development collaboration
 - Infrastructure configuration
 - Local development
 - Multi-tier applications
 - PaaS, SaaS

###### See the [survey results for 2016](https://www.docker.com/survey-2016)

---

### Docker vs VMs (once again)

![Docker vs traditional Virtualization](https://insights.sei.cmu.edu/assets/content/VM-Diagram.png)

---

### Why are Docker Containers Lightweight?

![Why are Docker Containers lightweight?](http://sandortoth.github.io/docker-presentation/img/containerslightweight.png)

---

### The Docker architecture

![Docker architecture](https://docs.docker.com/engine/article-img/architecture.svg)
###### See more at [Understanding docker](https://docs.docker.com/engine/understanding-docker/)

---

### Docker components

 - (Docker) client
 - daemon
 - engine
 - machine
 - compose
 - swarm
 - registry

---

### Docker client

It is the primary user interface to Docker. It accepts commands from the user
and communicates back and forth with a Docker daemon.

---

### Docker daemon

- It runs on a host machine. The user does not directly interacts with the daemon, but instead through the Docker client with the RESTful API or sockets.
- The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes.

---

### Docker engine

The daemon creates and manages Docker objects, such as images, containers, networks, and volumes.

![Docker Engine](http://sandortoth.github.io/docker-presentation/img/dockerengine.png)

---

### Docker machine

![Docker machine logo](http://sandortoth.github.io/docker-presentation/img/docker_machine.png)

A tool which makes it really easy to create Docker hosts on your computer,
on cloud providers and inside your own data center.
It creates servers, installs Docker on them, then configures the Docker client to talk to them.
Required for Mac, Windows users.

---

### Docker compose

![Docker compose logo](http://sandortoth.github.io/docker-presentation/img/docker_compose.png)

A tool for defining and running complex applications with Docker
(eg a multi-container application) with a single file.

---

### Docker swarm

![Docker swarm logo](http://sandortoth.github.io/docker-presentation/img/docker_swarm.png)

A native clustering tool for Docker. Swarm pools together several Docker
hosts and exposes them as a single virtual Docker host. It scale up to multiple hosts.

---

### Docker distribution

![Docker distribution logo](http://sandortoth.github.io/docker-presentation/img/docker_distribution.png)

A (hosted) service containing repositories of images which responds to the Registry API.

---

### The docker image
![ubuntu:15.04 image](https://docs.docker.com/engine/userguide/storagedriver/images/image-layers.jpg) 
#### An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization. Each instruction in a Dockerfile creates a layer in the image.

---

### The docker container
![container using ubuntu:15.04 image](https://docs.docker.com/engine/userguide/storagedriver/images/container-layers.jpg)
##### A container is a runnable instance of an image. A container is defined by its image as well as any configuration options you provide to it when you create or run it.

---

### The Dockerfile

> A Dockerfile is a text document that contains all the commands a user could call on the command line to create an image.

 - [Dockerfile with inline comments](https://github.com/sandortoth/sandortoth.github.io/blob/master/docker-presentation/examples/dockerfile/Dockerfile) just for education
 - [Dockerfile reference](https://docs.docker.com/engine/reference/builder/) on docker docs

---

### Common Docker Commands

```
// General info
man docker // man docker-run
docker help // docker help run
docker info
docker version
docker network ls

// Images
docker images // docker [IMAGE_NAME]
docker pull [IMAGE] // docker push [IMAGE]

// Containers
docker run
docker ps // docker ps -a, docker ps -l
docker stop/start/restart [CONTAINER]
docker stats [CONTAINER]
docker top [CONTAINER]
docker port [CONTAINER]
docker inspect [CONTAINER]
docker inspect -f "{{ .State.StartedAt }}" [CONTAINER]
docker rm [CONTAINER]

```

---

### Docker examples

- SSH into a container
- Build an image
- Docker [Volume](https://docs.docker.com/engine/userguide/containers/dockervolumes/)
- [Linked](https://docs.docker.com/engine/userguide/networking/default_network/dockerlinks/) containers
- Using [docker-compose](https://docs.docker.com/compose/)
- Scale containers with docker-compose
- Share an image (share this presentation)
- Package an app with its environment

---

### Example: SSH into a container

```
docker pull ubuntu
docker run -it --name ubuntu_example ubuntu /bin/bash
```

---

### Example: Build an Image

Let's build a [jenkins image](https://github.com/komljen/dockerfile-examples/blob/master/jenkins/Dockerfile)

```
cd ~/Docker-presentation
git clone git@github.com:komljen/dockerfile-examples.git.git
cd dockerfile-examples/jenkins
docker build -t jenkins-local .

// Test it
docker run -d -p 8099:8080 --name jenkins_example jenkins-local
// Open http://localhost:8099
```

---

### Example: Docker volume

Let's use [Apache server](https://bitbucket.org/EdBoraas/apache-docker/src/)

```
cd ~/Docker-presentation
mkdir apache-example
cd apache-example

docker pull eboraas/apache
docker run --name apache_volume_example \
           -p 8180:80 -p 443:443 \
           -v $(pwd):/var/www/ \
           -d eboraas/apache

// Locally create an index.html file
mkdir html
cd html
echo "It works using mount." >> index.html

// Open http://localhost:8180 to view the html file
```

---

### Example: Docker link containers

Let's create a [Drupal app](https://hub.docker.com/_/drupal/) (apache, php, mysql, drupal)

```
cd ~/Docker-presentation
mkdir drupal-link-example
cd drupal-link-example

docker pull drupal:8.0.6-apache
docker pull mysql:5.5

// Start a container for mysql
docker run --name mysql_example \
           -e MYSQL_ROOT_PASSWORD=root \
           -e MYSQL_DATABASE=drupal \
           -e MYSQL_USER=drupal \
           -e MYSQL_PASSWORD=drupal \
           -d mysql:5.5

// Start a Drupal container and link it with mysql
// Usage: --link [name or id]:alias
docker run -d --name drupal_example \
           -p 8280:80 \
           --link mysql_example:mysql \
           drupal:8.0.6-apache

// Open http://localhost:8280 to continue with the installation
// On the db host use: mysql

// There is a proper linking
docker inspect -f "{{ .HostConfig.Links }}" drupal_example
```

---

### Example: Using Docker Compose

Let's create a Drupal app with [docker-compose.yml](https://github.com/sandortoth/sandortoth.github.io/blob/master/docker-presentation/examples/docker-compose/docker-compose.yml)

```
cd ~/Docker-presentation
git clone git@github.com:sandortoth/docker-presentation.git
cd docker-presentation/examples/docker-compose

// Run docker-compose using the docker-compose.yml
cat docker-compose.yml
docker-compose up -d
```

---

### Example: Share a public Image

```
cd ~/Docker-presentation
git clone git@github.com:sandortoth/docker-presentation.git
cd docker-presentation

docker pull nimmis/alpine-apache
docker build -t tplcom/docker-presentation .

// Test it
docker run -itd --name docker_presentation \
           -p 8480:80 \
           tplcom/docker-presentation

// Open http://localhost:8480, you should see this presentation

// Push it on the hub.docker.com
docker push tplcom/docker-presentation
```

---

### Example: Export/Save/Load etc

```
docker pull nimmis/alpine-apache
docker run -d --name apache_example \
           nimmis/alpine-apache

// Create a file inside the container.
// See https://github.com/nimmis/docker-alpine-apache for details.
docker exec -ti apache_example \
            /bin/sh -c 'mkdir /test && echo "This is it." >> /test/test.txt'

// Test it. You should see message: "This is it."
docker exec apache_example cat /test/test.txt

// Commit the change.
docker commit apache_export_example myapache:latest

// Create a new container with the new image.
docker run -d --name myapache_example myapache

// You should see the new folder/file inside the myapache_example container.
docker exec myapache_example cat /test/test.txt

// Export the container as image
cd ~/Docker-presentation
docker export myapache_example > myapache_example.tar

// Import a new image from the exported files
cd ~/Docker-presentation
docker import myapache_example.tar myapache:new

// Save a new image as tar
docker save -o ~/Docker-presentation/myapache_image.tar myapache:new

// Load an image from tar file
docker load < myapache_image.tar

```

---

### Docker tips

There are known best practices (see a list at [examples/tips](https://github.com/sandortoth/sandortoth.github.io/blob/master/docker-presentation/examples/tips))

- Optimize containers (check [fromlatest.io](https://www.fromlatest.io/) and [imagelayers.io](https://imagelayers.io))
- Create your own tiny base
- Containers are not Virtual Machines
- Full stack Images VS 1 process per Container
- Create your private registry
- Create shortcut commands
- Use docker-compose.yml templates (see why at [lorry.io](https://lorry.io/))
- Be aware of the hub.docker.com docker agent version

---

### The Docker war

| Type | Software |
|:----:|----------|
| Clustering/orchestration | [Swarm](https://docs.docker.com/swarm/), [Kubernetes](http://kubernetes.io/), [Marathon](https://mesosphere.github.io/marathon/), [MaestroNG](https://github.com/signalfx/maestro-ng), [decking](http://decking.io/), [shipyard](http://shipyard-project.com/) |
| Docker registries | [Portus](http://port.us.org/), [Docker Distribution](https://github.com/docker/distribution), [hub.docker.com](http://hub.docker.com), [quay.io](https://quay.io), [Google container registry](https://cloud.google.com/tools/container-registry/), [Artifactory](https://www.jfrog.com/artifactory/), [projectatomic.io](http://www.projectatomic.io/) |
| PaaS with Docker | [Rancher](http://rancher.com/), [Tsuru](https://tsuru.io/), [dokku](https://github.com/dokku/dokku), [flynn](https://flynn.io/),  [Octohost](http://octohost.io/), [DEIS](http://deis.io/) |
| OS made of Containers | [RancherOS](http://rancher.com/rancher-os/) |

---

### Instead of Resources

 - [Awesome Docker](https://github.com/veggiemonk/awesome-docker) (list of Docker resources & projects)
 - [Docker cheat sheet](https://github.com/wsargent/docker-cheat-sheet)
 - [Docker in Practice](https://www.manning.com/books/docker-in-practice), [The Docker Book](http://www.dockerbook.com/) (books)
 - [Docker aliases/shortcuts](https://github.com/sandortoth/docker-presentation/tree/gh-pages/examples/shortcuts/docker-aliases.sh)
 - Docker [case studies](https://www.docker.com/customers)

---

### Questions?

[Review this presentation](https://)

###### In this presentation I have used [docker 1.11.1](https://github.com/docker/docker/releases/tag/v1.11.1) and [dry](https://github.com/moncho/dry).
###### Presentation material 'liberally borrowed' from [theodorosploumis](https://github.com/theodorosploumis/docker-presentation), [pointful](https://github.com/pointful/docker-intro)
###### and [Docker Inc.](https://www.slideshare.net/Docker/docker-birthday-3-intro-to-docker-slides). Thanks guys!


---
