# nginx-ingress-cert-manager-acme

REF: https://kubernetes.io/docs/tasks/access-application-cluster/ingress-minikube/

# Step 1: Enable ingress 
# Step 2: Install cert-manager
```
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.11.0/cert-manager.yaml
```
# Step 3: Create cluster-issuer
# Step 4: Create Ingress-Resources

# Production certificate issuer URL
```
server: https://acme-v02.api.letsencrypt.org/directory
```
# Initial password for argocd #admin
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```
