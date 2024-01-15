# Introduction

This repository contains the required scripts to deploy the **Mintik** backend services into your own server. It also contains the client app binaries that will be used for alpha testing.

# Prerequisites

Before jumping into the actual deployment process, let us make sure that you have the following setup:

**On the deployment server:**

- Your server can be either a physical machine or a Virtual Machine, running any Linux distro but preferably Ubuntu 22.04.3 LTS, or WSL in case of Windows. 
- Your server has Docker 24.0.5 (or higher) installed. Follow this document to install it with Snap on Ubuntu: https://snapcraft.io/install/docker/ubuntu
- You are running a Portainer instance on your server, this software is useful to easily monitor and manage Docker containers. To install it, run the following command on the server terminal (after installing docker), then you should be able to reach the Portainer page at http://your-server-ip:9000/. It will ask you to configure a password.

`sudo docker run -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer`

- Your server shall be reachable by client computers in your network and the port you choose to run the Mintik services shall be allowing traffic, check your firewalls.
