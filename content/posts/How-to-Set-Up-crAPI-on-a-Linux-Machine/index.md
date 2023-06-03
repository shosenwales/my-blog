--- 
draft: false
date: 2023-06-03
title: "How to Set Up crAPI on a Linux Machine"
description: "A tutorial on how to set up crAPI on a Linux machine."
slug: ""
authors: "Shuaib Oseni"
tags:
- application security
- api security
images:

  - url: hero.png
    alt: cover image
categories: ""
externalLink: ""
series: ""
---
![Cover Image](hero.png)

[crAPI](https://owasp.org/www-project-crapi/) (Completely Ridiculous API) is an intentionally vulnerable API that can be used to learn about and practice API security. It is an open-source project by [Open Worldwide Application Security Project (OWASP](https://owasp.org/)[)](https://owasp.org/), designed around the ten most critical [API](https://owasp.org/www-project-api-security/) security risks.

In this tutorial, you will learn how to set up crAPI on a Linux machine.

# Prerequisite 

To follow along in this tutorial, you must have the following:

- Basic knowledge of the terminal.
- Linux machine — This article uses Kali distribution

# Setting up crAPI

To set up crAPI, you create a directory called `labs` in your home directory.


    cd ~
    mkdir labs
    cd labs

Next, you need to clone the crAPI application by running the following command:


    git clone https://github.com/OWASP/crAPI.git

Before you can run the application, you need to install `docker.io` and `docker-compose`. To do that, run the following command in your terminal:


    #installing docker.io
    sudo apt install docker.io
    #installing docker-compose 
    sudo apt install docker-compose

Note: if you get the `unable to fetch some archives` error, run the command: `sudo apt update --fix-missing`. Then run the docker.io and docker-compose command one more time.

Now, you can navigate to the crAPI directory:


    cd ~/labs/crAPI/deploy/docker

Next, you can spin up the application by running the following command:


    sudo docker-compose up

Finally, you can view the application in your browser by visiting `localhost:8888`

![crAPI homepage](https://paper-attachments.dropboxusercontent.com/s_19FD3CEF828680C872463745C98B376CD411D3117E3D7DDA44F7F639D7B77FB8_1685788441195_crapi.png)


crAPI also comes with a mail server, which can be accessed by visiting `localhost:8025`

![mailhog](https://paper-attachments.dropboxusercontent.com/s_19FD3CEF828680C872463745C98B376CD411D3117E3D7DDA44F7F639D7B77FB8_1685788497368_mailhog.png)

# Conclusion

This tutorial explained crAPI and taught how to set it up on a Linux machine.
