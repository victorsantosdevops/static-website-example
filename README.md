# Simple Static WebSite

This project was created for the Hotmart DevOps test.


## Solution
To illustrate the deployment automation test in a dockerized environment, using the AWS CodePipeline, the master branch has different content than the dev branch, because simultaneously we will have the resolution of a prod.your-domain.com domain for a cluster container based on master branch and another container from the same dev.your-domain.com cluster based on the dev branch.

So that we can have a PROD / DEV environment with CI / CD based on GitHub branches.

Branch Master you see "PROD ENV"

![Image description](https://i.ibb.co/mcf9tD8/Screen-Shot-2020-07-22-at-04-48-15.png")

Branch dev you see "DEV ENV"

![Image description](https://i.ibb.co/w722rtH/Screen-Shot-2020-07-22-at-04-48-25.png)

## Setup your enviroment and run application
### Setup Enviroment

First you can install and update Docker from the repository. Follow the instructions below to install the Docker CE.

https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository


### Go to the link below and install Docker according to your operating system.

https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository

### Install Project
Go to your desired workstation folder and clone the repository

    git clone git@github.com:victorsantosdevops/static-website-example.git


### Docker RUN
Still on the terminal, in the root folder, run docker to make project access available locally and with you reflect any changes you make to the real-time code use the "developer mode Docker RUN"

    Build first to create a image
    "sudo docker build -t testwebsite ."
    
    Simple Docker RUN
    "sudo docker run -it -p 4000:80 testwebsite"
    
    
    Developer mode to Docker Run
    "sudo docker run -it -p 4000:80 -v "$(pwd):/app" -w "/app" testwebsite"