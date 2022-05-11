# microservices-test

This repository is used to understand how to design microservices and how they talk to each other using minikube.

The structure of the application is that we are building a distributed services cluster which is

The structure of the application is:

![project_structure](./project_structure.png)

- Auth Service: This service is responsible for granting JWT tokens which allow the user access to other services via the gateway service.
  - For authentication we're using a basic authentication mechanish of username and password.
  - This will be carried out by using `Authorization: Basic <credential>` which contains a base64(username:password) configuration in the request headers.
  - Upon successful authentication, we're sending back valid JWTs from the auth service back to the client.
