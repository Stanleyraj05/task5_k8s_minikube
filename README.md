# Task 5 – Kubernetes with Minikube

## Objective
Deploy and manage applications in a Kubernetes cluster using Minikube.

## Steps Performed

1. **Installed Minikube and kubectl**.
2. **Started Minikube Cluster**:
   ```bash
   minikube start
   ```
3. **Created a Deployment** using `deployment.yaml`:
   ```bash
   kubectl apply -f deployment.yaml
   ```
4. **Exposed the Application** using `service.yaml`:
   ```bash
   kubectl apply -f service.yaml
   ```
5. **Verified Pods and Services**:
   ```bash
   kubectl get pods
   kubectl get services
   ```
6. **Scaled the Deployment**:
   ```bash
   kubectl scale deployment myapp-deployment --replicas=3
   ```
7. **Described Resources for Logs and Status**:
   ```bash
   kubectl describe deployment myapp-deployment
   ```

## Outcome
Successfully deployed, exposed, and scaled an application on a local Minikube cluster.

## Files Included
- `deployment.yaml` – Kubernetes deployment configuration
- `service.yaml` – Kubernetes service definition
- `README.md` – Documentation of the task
