# lab

ArgoCD Install

kubectl apply -k https://github.com/argoproj/argo-cd/manifests/crds\?ref\=stable

kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d