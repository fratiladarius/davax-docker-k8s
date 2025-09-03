# davax-docker-k8s

hello world app in flask, containerized with docker and deployed on kubernetes.

## docker
```bash
cd docker
docker build -t hello-flask:1 .
docker run -p 8000:8000 hello-flask:1
curl http://localhost:8000
```

## kubernates
```bash
kubectl apply -f k8s/
kubectl get pods,svc
kubectl port-forward svc/hello-svc 8000:8000
curl http://localhost:8000
```

## cleanup
```bash
docker rm -f hello
kubectl delete -f k8s/
```
