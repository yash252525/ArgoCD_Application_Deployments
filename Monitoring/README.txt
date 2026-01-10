ArgoCD by default exposes metrics
find out using k get svc -n argocd
1. argocd-applicationset-controller -> 8082/metrics
2. argocd-server -> 8083/metrics
3. argocd-repo-server -> 8084/metrics

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
kubectl create namespace monitoring
helm install kube-prometheus-stack prometheus-community/kube-prometheus-stack -n monitoring

apply metrics.yml and expose the ports.
