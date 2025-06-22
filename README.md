# Kubernetes Full Stack Setup with NGINX, Redis, MySQL & phpMyAdmin

This project sets up a simple full stack environment on Kubernetes, consisting of:

- **NGINX** – Static web server
- **Redis** – In-memory data store
- **MySQL** – Database service
- **phpMyAdmin** – Web UI for managing the MySQL database

> ✅ Built to run on Minikube or any VM-hosted Kubernetes cluster  
> ✅ No hardcoding — uses Secrets for credentials  
> ✅ Neatly organized for GitHub and team collaboration

---

## 📁 Folder Structure
k8s-app/
├── nginx/    -used Nodeport
├── redis/     -used Clusterip
├── mysql/
│ └── secret.yaml
├── phpmyadmin/
├── README.md
└── .gitignore