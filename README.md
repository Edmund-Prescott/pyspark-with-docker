# Using PySpark with Docker!
Setup a PySpark work environment with Docker (and Vs Code).

## Table of Contents
1. [Introduction](#introduction)
2. [Docker Setup](#Docker-Setup)
3. [Setup Pyspark Environment with Docker](#Setup-Pyspark-Environment-with-Docker)\
4. [Using Pyspark with VS Code](#Using-Pyspark-with-VS-Code)

## Introduction
When I was first introduced to using PySpark I found the installation process to be unintuitve. Docker and Dockerhub enable an intuitive installation process to quickly setup a PySpark work environment.

## Docker Setup
Before getting started, make sure Docker is installed on your machine. If not, it can be download here. https://www.docker.com/products/docker-desktop/
Here's the official documentation for installing Docker https://docs.docker.com/engine/install/ 
> :bulb: **Tip:** _I've had some troubles setting up Docker in the past, if Docker engine keeps shutting down upon booting up uninstalling and reinstalling has fixed the issue for me._

### Docker on Windows
If you work on Windows operating system like I do you'll need to download a Linux Subsystem for Windows (WSL) to use Docker. You can install a WSL through the commandline ```wsl --install```

## Setup Pyspark Environment with Docker
To configure PySpark in your Docker environment pull the pyspark-notebook form the Jupyter repository on Docker Hub.
```
docker run --name pyspark -p 8888:8888 jupyter/pyspark-notebook
```
This command will install the jupyter/pyspark-notebook image if it's not already installed and run a container based on this image called pyspark.
To access the notebook in this container click on the url that should now be in the commandline, it should look something like: http://127.0.0.1:8888/
> :bulb: **Tip:** _The url will be in the container logs which can be accessed with ```docker logs pyspark```_

## Hello World
PySpark should now be configured and ready to use! Try running PySpark code in the Jupyter lab to confirm the installation.

## Using Pyspark with VS Code
Integrating PySpark with Visual Studio Code (VS Code) provides a powerful development environment.

## Install Vs Code Extensions
- Docker
- Jupyter

Create a Jupyter notebook in your repository and run all cells. Vs Code will prompt you for a kernal.
Select Existing Jupyter Server and input the url from earlier.
Vs Code will then prompt you for a password, the password is the token attached to the url.




