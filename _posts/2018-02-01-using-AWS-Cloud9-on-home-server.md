---
published: false
layout: post
excerpt: Setting up AWS Cloud9 on your home server
permalink: /using-AWS-Cloud9-on-home-server
---
## Setting up AWS Cloud 9 to ssh to your home Ubuntu server

### Prepare your home Ubuntu server

- Set up port forwarding on your home router. You want to forward tcp port 22. Ideally, you want to forward it to non-standard port (say, 2220). For now, to keep things simple (but perhaps insecure), I just forwarded it to 22. The process for doing this is router-specific. As part of doing this, you also have to reserve the IP address for your 

- Get the public ip address of your machine. There are several ways to do this: 
```shell
wget -qO- http://ipecho.net/plain ; echo
curl ipinfo.io/ip
```

- Install nodejs on your home server:
```shell
curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
sudo apt-get install -y nodejs
```

- Set up permissions on your home directory:
```
sudo chmod u=rwx,g=rx,o=rx ~
```

- You need to have python v2.7 in your path (check how critical this requirement is and what happens if you have version v3.x instead)

### Setup on AWS

- Login to your AWS console at https://console.aws.amazon.com/cloud9/home?region=us-east-1 (or appropriate region)

- Click "Create Environment"
