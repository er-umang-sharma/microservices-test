# Steps to build and deploy the container to the kube9 local k8s cluster

## Building & Pushing the image to Docker Hub

* Go to the auth directory
* Run the command `docker build .`
* After the container is biult, run the command `docker tag <image-tag> umangsh454/microservice-test-auth:latest`
* Once the image is tagged you can run the command to push this image to the docker hub: `docker push umangsh454/microservice-test-auth:latest`

## Starting the minikube environment

* Run the command `minikube start`

## Deploying the updated code to the minikube kubernetes cluster

* Go to the manifest directories where the kubernetes config files are stored.
* Run the command: `kubectl apply -f ./`

The above steps will delpoy the updated code to the local minikube cluster.
