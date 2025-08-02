# ArgoCD

## Install
kubectl create namespace argocd\nkubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get ns
kubectl get po -n argocd -w
kubectl get svc -n argocd 
kubectl port-forward svc/argocd-server -n argocd 8080:443
kubectl get -n argocd secret argocd-initial-admin-secret -o yaml