# Introduction

This repository contains the required scripts to deploy the **Mintik** backend services into your own server. It also contains the client app binaries that will be used for alpha testing.

# Prerequisites

Before jumping into the actual deployment process, let us make sure that you have the following setup:

**On the deployment server:**

- The server can be either a physical machine or a Virtual Machine, running any Linux distro but preferably Ubuntu 22.04.3 LTS, or WSL in case of Windows. 
- The server needs Docker 24.0.5 (or higher) installed. Follow this document to install it with Snap on Ubuntu: https://snapcraft.io/install/docker/ubuntu
- You need to run a [Portainer](https://www.portainer.io/ "Portainer") instance on your server, this software is useful to easily monitor and manage Docker containers. To install it, run the following command on the server terminal (after installing docker), then you should be able to reach the Portainer page at http://your-server-ip:9000/. It will ask you to configure a password.

`# sudo docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer`

- Your server shall be reachable by client computers in your network and the port you choose to run the Mintik services shall be allowing traffic, double check your firewalls or anything else that could be blocking traffic between clients and server.
- Clone or download this repository to your server.

**On your local machine**

- Your local machine shall be running Windows 10 or higher.
- Install [MongoDB Compass](https://www.mongodb.com/products/tools/compass "MongoDB Compass") 1.40.4 or higher. We will use it to access the MongoDB database. 

# Deploying backend services

Clone or download this repository to your server:

`# git clone https://github.com/scazaresm/mintik-deployment.git`

Navigate in your terminal to the services directory on this repo:

`# cd mintik-deployment/services`

Deploy the docker compose file:

`sudo docker-compose up -d`

That's it, you should be able to see the Docker containers are running, either from the terminal or from the Portainer web interface:

`sudo docker ps`


