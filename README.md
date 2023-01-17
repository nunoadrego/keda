# keda
Playing with Keda

## Create K8s cluster and install Keda with helm

```
minikube start --kubernetes-version v1.24.9
```

```
helm repo add kedacore https://kedacore.github.io/charts
helm repo update
helm install keda kedacore/keda --namespace keda --create-namespace --context minikube
```

## Create Deployment and ScaledObject
```
k apply -f deploy-so.yaml --context minikube
```
