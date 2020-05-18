# DockerProject_IIEC

# Introduction to this project
In this project, we have created a complete wordpress website infrastructure with mysql as a database using docker container technology. With the help of this project, you can simply run a complete wordpress website within few clicks.

# Requirements
1. Redhat OS
2. Docker

# Docker 
Docker is a set of platform as a service (PaaS) products that uses OS-level virtualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries and configuration files they can communicate with each other through well-defined channels. All containers are run by a single operating system kernel and therefore use fewer resources than virtual machines.

# Installing Docker

I have used Red Hat Linux Version 8 for installing docker. If you have redhat subscription, simply run the following command

> yum install docker-ce

else you can use other method to install docker. 

Firstly, create a yum repo having docker url to download.

Then change the directory to `/etc/yum.repos.d/` and create a new file named `docker.repo` and put the following code. Using `docker` as my repo name, it would look like
```
[docker]
baseurl="https://download.docker.com/linux/centos/7/x86_64/stable/"
gpgcheck=0
```
then install docker by running the command `yum install docker-ce --nobest`

# Using Docker
After installing docker, you need to start docker service first. For starting docker, run this command `service systemctl start docker.service` and to automatically start docker sevice after system reboot, use `systemctl enable docker.sevice`

## Required files to download
I am using specific version to work with. You can change the version as per your preference

- Wordpress : wordpress:5.1.1-php7.3-apache   `docker pull wordpress:5.1.1-php7.3-apache`
- MySql : mysql:5.7   `docker pull mysql:5.7`

Now, goto the directory where your docker-compose file is and run the command for starting complete infrastructure `docker-compose start`. 
Now everything is completely set, type your system's IP with port number `8082`. As, I have used port `8082` in my project, you can change it according to your system's availability.

#Vimal_daga #IIEC_RISE #IIEC_DOCKER #RightMentor #RightEducation
