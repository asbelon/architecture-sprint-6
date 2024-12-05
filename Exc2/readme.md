```bash
minikube start --vm-driver=hyperv
```

[log](./worklogs/01.log)

```bash
kubectl version --client
```

[log](./worklogs/02.log)

```bash
minikube start --addons=metrics-server 
```

[log](./worklogs/03.log)

```bash
minikube addons enable metrics-server
```

[log](./worklogs/04.log)

```bash
kubectl get pods --all-namespaces
```

[log](./worklogs/05.log)

```bash
kubectl get deployment metrics-server -n kube-system
```

[log](./worklogs/06.log)

```bash
kubectl describe deployments
```

```bash
kubectl apply -f deployment.yaml
```

```bash
kubectl apply -f service.yaml
```

```bash
minikube dashboard
```

```bash
watch kubectl get all
```

```bash
kubectl get services
```

[log](./worklogs/07.log)

```bash
kubectl describe services/testapp-service
```

```bash
minikube service testapp-service --url 
```

[log](./worklogs/08.log)

[http://172.27.73.254:30951](http://172.27.73.254:30951)

```bash
minikube service testapp-service --url 
```

```bash
kubectl apply -f hpa.yaml
```

```bash
kubectl get hpa
```

[log](./worklogs/09.log)