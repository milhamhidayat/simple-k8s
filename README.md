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
``

## Deployment

There are two
* Imperative deployment - do these steps to arrive this container setup
* Declarative deployment - container setup should look like this, make it happen