# Kubernetes Full Stack Setup with NGINX, Redis, MySQL & phpMyAdmin

This project sets up a simple full stack environment on Kubernetes, consisting of:

- **NGINX** – Static web server
- **Redis** – In-memory data store
- **MySQL** – Database service
- **phpMyAdmin** – Web UI for managing the MySQL database

> ✅ Built to run on Minikube or any VM-hosted Kubernetes cluster  
> ✅ No hardcoding — uses Secrets for credentials  


---

## 📁 Folder Structure
- k8s-app/
- ├── nginx/    -used Clusterip
- ├── redis/     -used Clusterip and redis default port 6379
- ├── mysql/
- │ └── secret.yaml
- ├── phpmyadmin/   
- ├── README.md
- └── .gitignore

## - **NGINX** - 
kubectl logs -l app=nginx   -used to check if nginx is serving a page
minikube service nginx-service  -this was used to view the nginx welcome page
## Apply all deployments and services
kubectl apply -f ./nginx/
kubectl apply -f ./redis/
kubectl apply -f ./mysql/
kubectl apply -f ./phpmyadmin/
## Accessing the webpage
kubectl port-forward svc/phpmyadmin-service 8085:80

