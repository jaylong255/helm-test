# Helm Test

## Command Reference

### Start Minikube
```sh
minikube start
```

### Switch Context from OpenShift to Minikube
```sh
kubectl config use-context minikube
```

### List all Namespaces
```sh
kubectl get namespaces
```

### Select Namespace
```sh
kubectl config set-context --current --namespace=helm-test
```

### Show all resources for a namespace
```sh
kubectl get all
```

### Delete Namespace
```sh
kubectl delete namespace helm-test
```


## Primary Chart

### Chart
```yaml
# Chart.yaml

# Name of the chart
name: nginx-server

# Version of the chart
version: 1.0.0

# Applicaiton type
appVersion: "latest"

# Dependencies (empty for this chart)
dependencies: []

# Description of the chart
description: A simple Nginx web server deployment
```


```sh
helm install wordpress ./wordpress
helm dependency build
helm repo update
```