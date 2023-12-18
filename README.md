# k8s-service-discovery-demo
A C# sample app that shows tha use of Kubernetes REST API to perform service discovery of API endpoints 

### Design
![image](https://github.com/madhub/k8s-service-discovery-demo/assets/8907962/e792cafa-c569-42f4-bb4b-084519c67cde)



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

