# Docker Ngnix PHP 8
Docker Image made for a project startup using ngnix with php 8.

If you need more help working with docker, please check the official documentation in
[https://docs.docker.com/](https://docs.docker.com/).

## Build and preview locally

On your local machine, clone this repo:

```bash
git clone https://github.com/lickybuay/docker-nginx-php.git
cd docker-nginx-php
```

Then build and run the documentation with [Docker Compose](https://docs.docker.com/compose/)

```bash
docker-compose up -d --build
```

> Docker Compose is included with [Docker Desktop](https://docs.docker.com/desktop/).
> If you don't have Docker Compose installed, [follow these installation instructions](https://docs.docker.com/compose/install/).

Once the container is built and running, visit [http://localhost:8080](http://localhost:8080)
in your web browser to view the docs.

To rebuild the docs after you made changes, run the `docker-compose up` command
again. This rebuilds the documentation, and updates the container with your changes:

```bash
docker-compose up -d --build
```

Once the container is built and running, visit [http://localhost:8080](http://localhost:8080)
in your web browser to view the docs.


To stop the staging container, use the `docker-compose down` command:

```bash
docker-compose down
```

Once the container is built and running, visit [http://localhost:8080](http://localhost:8080)
in your web browser to view the docs.


## Important files

- `/config/nginx/default.conf` define default config for nginx
- `/config/php/php.ini` define php configuration in php
- `/config/docker` docker configuration of all the commands a user could call on the command line to assemble an image

### Other PHP versions

If you need to change the php version just modify Dockerfile to the version you need (Only tested php 7.1 and 8.0.11) 

From
```bash
$ php:8.0.11-fpm
```
To
```bash
$ php:php:7.1-fpm
```
