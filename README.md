# ngrok Demo

_CodingBerlin Hands-On Meetup (2017-09-20)_

This is a demo for ngrok tunnels.

### Requirements

For usage with Docker:

- Docker CE  
  [HowTo for Ubuntu](https://docs.docker.com/engine/installation/linux/ubuntu/#install-using-the-repository)   
  [HowTo for MacOS](https://docs.docker.com/docker-for-mac/install/) 
- docker-compose  
  [HowTo for Ubuntu](https://docs.docker.com/compose/install/)   
  [HowTo for MacOS](https://docs.docker.com/docker-for-mac/install/) 
  
For usage with Vagrant:

- [Vagrant](https://www.vagrantup.com/downloads.html)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


## Setup

- Clone repository
  ```
  git clone https://github.com/coding-berlin/hands-on-ngrok/
  cd hands-on-ngrok
  ```

- Run setup 
  - for Docker
    ```
    docker-compose up -d
    ```
  - for Vagrant
    ```
    vagrant up
    ```
    
To verify your installation, open a browser tab
- for Docker setup:  http://localhost/
- for Vagrant setup: [http://192.168.99.99/](http://192.168.99.99/)     

## Demos

To run the demos, you have to open a shell. 

- with Docker
```
docker exec -ti handsonngrok_php-apache_1 /bin/bash 
```
- with Vagrant
```
vagrant ssh
```

### Start simple HTTP tunnel directly

```
ngrok http 80
```  

### Start simple HTTP tunnel from config

```
ngrok start test-basic
```  

### Start HTTP tunnel with authentication

```
ngrok start test-auth
```  
Login: `demo`/`secret`


### Start multiple HTTP tunnels from config

```
ngrok start test-basic test-auth test-no-inspect
```  

## Web interface

ngrok provides a webinterface to inspect current tunnels:

[http://0.0.0.0:4040](http://0.0.0.0:4040)

## Links

- ngrok website: https://ngrok.com/  
- ngrok configuration: https://ngrok.com/docs#tunnel-definitions

