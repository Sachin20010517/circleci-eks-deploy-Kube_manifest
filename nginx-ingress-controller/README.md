# NGINX Ingress Controller Setup

## Introduction

The NGINX Ingress Controller is a Kubernetes controller that manages access to services in a Kubernetes cluster. It uses NGINX as a reverse proxy and load balancer to route external traffic to your services.

## Installation

### Prerequisites

- Kubernetes cluster (e.g., EKS, GKE, or a local cluster like Minikube)
- `kubectl` command-line tool installed and configured to access your cluster

### Steps to Install NGINX Ingress Controller

1. **Create a Namespace for Ingress:**

   ```bash
   kubectl create namespace ingress-nginx
   ````
2. **Install NGINX Ingress Controller:**

   ```bash
   kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.12.0/deploy/static/provider/aws/deploy.yaml
   ````
3. **Check that the NGINX Ingress Controller pods are running:**

   ```bash
    kubectl get pods -n ingress-nginx
   ````

 ### Troubleshooting ###

1. **Checking Logs of the ingress-nginx-controller- pod::**

   ```bash
   kubectl logs <nginx-ingress-controller-pod-name> -n ingress-nginx
   ````
