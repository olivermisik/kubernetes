# Kubernetes Nasadenie so Secret, Service, HPA, PDB a Service Account

## Prehľad krokov:
    1. Nainštalujte Minikube 
    2. Aplikujte Kubernetes manifesty: Deployment, Service, HPA, PDB a Service Account
    3. Overte nasadenie a monitorujte aplikáciu

## Aplikovanie manifestov:
    kubectl apply -f serviceaccount.yaml
    kubectl apply -f secret.yaml
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    kubectl apply -f hpa.yaml
    kubectl apply -f pdb.yaml

## Manuálne kroky:
    Spustenie Minikube -> minikube start
    Sprístupnenie aplikácie cez NodePort -> minikube service nginx-service
    Overenie Rolling Update -> 
        kubectl set image deployment/nginx-deployment nginx=nginx:1.21.6
        kubectl rollout status deployment/nginx-deployment
    Správanie PDB -> kubectl get pdb
