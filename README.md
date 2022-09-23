![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23000000.svg?style=for-the-badge&logo=npm&logoColor=white)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![SolidJS](https://img.shields.io/badge/SolidJS-2c4f7c?style=for-the-badge&logo=solid&logoColor=c8c9cb)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)

# SolidJS Maven Build

A sample project to show how you can integrate a npm build into your maven infrastructure.
The result of the maven build is the dist directory placed in the target directory. From there on the Dockerfile uses it to build a container.
Feel free to use this a basis for your project, maybe as a submodule besides your other modules?

# Getting started

As you might expect you need Java and Maven installed on your system to build the app.
The example is based on Java 11, Maven 3.8.6 and NodeJS 16.17.0, Vite 3.1.3 and SolidJS 1.5.1.  
To build an NodeJS application with Maven the Frontend Maven Plugin is used and will automatically download NodeJS and perform the build process.

Simply run:
``
mvn clean install
``  
After that you can build the container:
``
docker build -t solidjs-maven-build:latest .
``  
And finally run it:
``
docker run -p 3000:80 solidjs-maven-build:latest
``

# Software

* [Java 11 (Amazon Coretto)](https://docs.aws.amazon.com/de_de/corretto/latest/corretto-11-ug/downloads-list.html)
* [Maven](https://maven.apache.org/download.cgi)
* [Frontend Maven Plugin](https://github.com/eirslett/frontend-maven-plugin)
* [NodeJS](https://nodejs.org/en/)
* [Docker](https://www.docker.com/products/docker-desktop/)