# Enable ingress 
Enable ingress in Minikube

```sh
minikube addons enable ingress
```
Creates simple echo-server services and an Ingress object to route to these services.
```sh
kubectl apply -f echo-server-services+ingress-object.yaml
```
This create an Nginx Ingress Class + an Ingress Object that route the traffic to the 2 Services that route traffic to the respective Pods

 