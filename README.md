# k8s-service-discovery-demo
A C# sample app that shows tha use of Kubernetes REST API to perform service discovery of API endpoints 

### Design
![image](https://github.com/madhub/k8s-service-discovery-demo/assets/8907962/63dd2f6e-e61f-4a58-84c3-0b77a2b396ac)


### Build
```shell
docker build --platform=linux/amd64 -t kube-sd-demo-server
```

### Running local K8S environment
```shell
kubectl apply -f k8s-deploy.yaml
```
Testiing
```shell
  curl -v -k -H "Content-Type: application/json" -d "{\"a\":\"b\" }" "https://kubernetes.docker.internal/api/demo/notify"
```

