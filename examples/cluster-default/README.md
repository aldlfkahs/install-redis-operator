## Prerequisites
- k8s cluster 환경 : 3개 이상의 worker node
- cluster size : 3이상

## Reference
- [redis-cluster](https://ot-container-kit.github.io/redis-operator/guide/redis-cluster-config.html#helm-parameters)

## Redis Cluster Installation Guide
### 1. namespace 생성
```shell
kubectl create namespace {원하는 namespace 명}
```
### 2. secret 생성
```shell
kubectl apply -f secret.yaml -n {생성한 namespace 명}
```

### 3. redis cluster 생성
```shell
kubectl apply -f cluster.yaml -n {생성한 namespace 명}
```

## 삭제 Guide
### 1. secret 삭제
```shell
kubectl delete -f secret.yaml -n {생성한 namespace 명}
```

### 2. redis cluster 삭제
```shell
kubectl delete -f cluster.yaml -n {생성한 namespace 명}
```