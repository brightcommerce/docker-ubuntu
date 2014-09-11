# Docker Ubuntu

Dockerfile to build an Ubuntu v14.04 base image for Docker containers. This image adds some essential tools such as wget, sudo, pwgen, unzip, logrotate, supervisor, net-tools, language-pack-en and software-properties-common.

## Table of Contents

- [Version](#version)
- [Installation](#installation)
- [How To Use](#how-to-use)
- [Credit](#credit)

## Version

The current release (v14.04.20140911) contains scripts to install Ubuntu 14.04 LTS (Trust Tahr), and uses the [official Ubuntu base image](https://registry.hub.docker.com/_/ubuntu/). Our version numbers will reflect the version of Ubuntu being installed.

## How To Use

This image is intended for use as the base image in app and service containers. At the top of your `Dockerfile` specify the `FROM` key:

``` bash
FROM brightcommerce/ubuntu:14.04.20140911
```

Alternatively, if you want to build the image yourself, pull the latest version of the image from the Docker Index. This is the recommended method of installation as it is easier to update the image in the future. These builds are performed by the **Docker Trusted Build** service.

``` bash
docker pull brightcommerce/ubuntu:14.04.20140911
```

Alternately you can build the image yourself:

``` bash
git clone https://github.com/brightcommerce/docker-ubuntu.git
cd docker-ubuntu
docker build -t="$USER/ubuntu" .
```

## Credit

This repository was based on the work of [docker-ubuntu by Sameer Naik](https://github.com/sameersbn/docker-ubuntu).
