## ☸️ kubernetes prometheus Setup


kubectl create namespace monitoring
kubectl create -f clusterRole.yaml
kubectl create -f config-map.yaml
kubectl create -f pvc-storageclass.yaml --namespace=monitoring
kubectl create -f pvc.yaml --namespace=monitoring
k get pvc -A
kubectl create  -f prometheus-deployment.yaml 
k get deployment -n monitoring
kubectl get deployments --namespace=monitoring
kubectl create -f prometheus-service.yaml --namespace=monitoring
k get all -A


Complete prometheus monitoring stack setup on Kubernetes.

Idea of this repo to understand all the components involved in prometheus setup.

You can find the full tutorial from here--> [Kubernetes Monitoting setup Using Prometheus](https://devopscube.com/setup-prometheus-monitoring-on-kubernetes/)

## 🚀 CKA, CKAD, CKS or KCNA Voucher Codes

If you are preparing for CKA, CKAD, CKS or KCNA exam, **get $57 discount** today using code **DCUBEOFFER** at https://kube.promo/latest. It is a limited time offer

## ✍️ Other Manifest repos

Kube State metrics manifests: https://github.com/devopscube/kube-state-metrics-configs

Alert manager Manifests: https://github.com/bibinwilson/kubernetes-alert-manager

Grafana manifests: https://github.com/bibinwilson/kubernetes-grafana

Node Exporter manifests: https://github.com/bibinwilson/kubernetes-node-exporter


