#Docker-Php

A VERY simple PHP / Apache container build along with the Kubernetes configuration file to run with Minikube. Tested in ARM64. 

##Requires;

1. Docker
```bash
docker -v
```
2. Minikube
```bash
minikube version
```

##To run as local image; 

```bash
#Start minikube
minikube start

#Get inside minikube docker env
eval $(minikube docker-env)

#Build the image
docker-compose build

#Create deployment and service
kubectl apply -f docker-php.yaml

#Serve the app
minikube service docker-php-service
```

###Thanks!