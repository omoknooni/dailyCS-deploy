# dailyCS-deploy
Repo for Deploy dailyCS

## Initial Setup
1. ArgoCD 설치
```
helm repo add argo https://argoproj.github.io/argo-helm

kubectl create namespace argo

# values.yaml : https://raw.githubusercontent.com/argoproj/argo-helm/main/charts/argo-cd/values.yaml

helm install argocd argo/argo-cd -f values.yaml -n argo
```
2. AppProject 추가, Root App 연결
```
kubectl apply -f root-app.yml -n argo
```