# simple-k8s
Simple k8s from kubernetes course

## Create object
```sh
kubectl apply -f <object manifest/config file>
```

Run
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