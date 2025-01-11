# Setting Up ArgoCD

1️⃣ **Create the ArgoCD Namespace**

```bash
kubectl create namespace argocd
````
2️⃣ Get All Namespaces to Confirm Creation
```bash
kubectl get namespaces

````
3️⃣ Install ArgoCD

```bash
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

````

4️⃣ Get Pods and Services in the ArgoCD Namespace

```bash
kubectl get pods -n argocd
kubectl get svc -n argocd
```

5️⃣ Port Forward the ArgoCD Server
```bash
kubectl port-forward svc/argocd-server 8080:443 -n argocd
````

6️⃣Get Secrets in the ArgoCD Namespace

```bash
kubectl get secrets -n argocd
kubectl edit secret argocd-initial-admin-secret -n argocd
````

7️⃣Decode the Initial Admin Password
```bash
echo ZlowekhCU1p2eXdrUDRPcg== | base64 --decode
````
