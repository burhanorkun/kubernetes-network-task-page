## Kubernete

Start a cluster using the docker driver:

> minikube start --driver=docker

To make docker the default driver:

> minikube config set driver docker

## Build images

In the every project directory, you can run:

> docker build -t burhanorkun/kub-demo-auth .

> docker build -t burhanorkun/kub-demo-users .

> docker build -t burhanorkun/kub-demo-tasks .

> docker build -t burhanorkun/kub-demo-frontend .

## Push images to the Docker Hub

> docker push burhanorkun/kub-demo-auth

> docker push burhanorkun/kub-demo-users

> docker push burhanorkun/kub-demo-tasks

> docker push burhanorkun/kub-demo-frontend

### kubernete apply

> kubectl apply -f=auth-deployment.yaml -f=auth-service.yaml

> kubectl apply -f=users-deployment.yaml -f=users-service.yaml
> kubectl apply -f=tasks-deployment.yaml -f=tasks-service.yaml

> kubectl apply -f=frontend-deployment.yaml -f=frontend-service.yaml

if you want to analyz your pod inside.

> kubectl logs [podname] -p

## Serve frontend service

> minikube service frontend-service

you can access your service on kubernetes proxy service
