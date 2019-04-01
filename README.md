# simple-k8s
Simple k8s from kubernetes course

## Create object
```sh
kubectl apply -f <object manifest/config file>
```

* create pod and services object
```sh
kubectl apply -f client-pod.yaml
kubectl apply -f client-node-port.yaml 
```

* Get Ip
```sh
minikube ip
```

* Access multi-client
```sh
<ip>:31515
```

* Get detailed info about an object
```sh
kubectl describe <object type> <object name>
```

## Deployment

- object controller to update or rollback pods & replica set
- maintain set of identical pods
- ensure have the correct config and the right number exists
- will monitor

There are two:
* Imperative deployment - do these steps to arrive this container setup
* Declarative deployment - container setup should look like this, make it happen

Delete pod
```sh
kubectl delete -f <config file>
```

## Update deployment

Open multi-docker-client

1. Build docker image
```sh
docker build -t <docker id>/<image name>:<tag> .
```

Example:
```sh
docker build -t photon628/multi-client:v5 .
```

2. Push to docker hub
```sh
docker push <docker id>/<image name>:<tag>
```

Example:
```sh
docker push photon628/multi-client:v5
```

3. Imperative command to update deployment image

```sh
kubectl set image <object-type>/<object-name> <container-name>=<new image to use>
```

Example:
```sh
kubectl set image deployment/client-deployment client=photon628/multi-client:v5
```

## Connect docker command to container inside kubernetes

```sh
eval $(minikube docker-env)
```

Simplify
```sh
minikube docker-env
```