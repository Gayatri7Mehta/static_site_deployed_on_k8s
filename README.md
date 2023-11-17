# static_site_deployed_on_k8s
This repository puts an emphasis on deploying a static site on Kubernetes cluster. The aim is to learn hands on on the orchestration DevOps tool"Kubernetes".

create a configMap:
kubectl create configmap static-site-config --from-file=index.html

kubectl commands:
minikube start
touch static-site-deployment.yaml
nano static-site-deployment.yaml
kubectl apply -f static-site-deployment.yaml
kubectl expose deployment static-site-deployment --type=NodePort --port=80
minikube service static-site-deployment --url


