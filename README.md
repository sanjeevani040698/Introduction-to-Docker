# Introduction-to-Docker

Containerization, as we say, is basically a lightweight virtualization. Docker is a software containerization platform. It provides abstraction of a operating system level virtualization.

As in virtualization, we distribute the resources here too but the isolation here is not as strict, hence lightweight. For example, in case of virtualization we allocate fixed amount of resources like RAM, memory, hardware etc., even if they remain unused in their area. This is the major drawback of virualization which presents great acknowledgement to containerization.

It is now emerging as a new technology to deploy applications as microservices. It allows the parts of a big software application to be implemented and deployed independently without intervening with each other or having to manage all at a time, hence lightens a developer's tasks.

Moreover, it facilitates easy carryout of different stages of a software development process by providing awesome kind of portability. Now the software tester, concerned with a particular application, does not need to worry about the environment in which the developer would have worked to build the application. A big headache already settled!


# docker pull

docker pull command can be used to pull certain already present images from the docker hub.

Docker hub is nothinng but a repository which contains large amount of heavily neede and used images which we can use my the pull command.

# Building our own Images

For this we need to have a Dockerfile, for the build code and and a folder containing the application to be deployed.

A simple example has been shown.

Dockerfile here:

FROM httpd:2.4

COPY ./public_html/ /usr/local/apache2/htdocs/ # public_html is the folder containing the application files


Build command: docker build -t image-name


Run command: docker run -p 8090:80 image-name

Note: Detailed explanation in Docker-Usecase
