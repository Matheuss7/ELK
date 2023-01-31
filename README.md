# Installation

Install storageclass
```console
kubectl apply -f storageclass.yaml
```
Install crds
```console
kubectl apply -f crds.yaml
```
Install operator
```console
kubectl apply -f operator.yaml
```
Install elasticsearch
```console
kubectl apply -f elasticsearch-deploy.yaml
```
Install kibana
```console
kubectl apply -f kibana-deploy.yaml
```
Install apm-server
```console
kubectl apply -f apm-server-deploy.yaml
```
Install heartbeat
```console
kubectl apply -f heartbeat-deploy.yaml
```

# Accessing kibana

Do port-forward in kibana service, and login with elastic credencials.

## User
User: elastic

## Password

Run the command below to get the secret value with the password
```console
echo PASSWORD=$(kubectl get -n elastic secret elasticsearch-es-elastic-user -o go-template='{{.data.elastic | base64decode}}')
```

