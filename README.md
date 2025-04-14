# Task 5 – Kubernetes with Minikube

## Objective
Deploy and manage applications in a Kubernetes cluster using Minikube.

## Steps Performed

1. **Installed Minikube and kubectl**.
2. **Started Minikube Cluster**:
   ```bash
   minikube start
   ```
3. **Created a ConfigMap** using `configmap.yaml`:
   ```bash
   kubectl apply -f configmap.yaml
   ```
4. **Created a Deployment** using `deployment.yaml`:
   ```bash
   kubectl apply -f deployment.yaml
   ```
5. **Exposed the Application** using `service.yaml`:
   ```bash
   kubectl apply -f service.yaml
   ```
6. **Verified Pods and Services**:
   ```bash
   kubectl get pods
   kubectl get services
   ```
7. **Scaled the Deployment**:
   ```bash
   kubectl scale deployment myapp-deployment --replicas=3
   ```
8. **Described Resources for Logs and Status**:
   ```bash
   kubectl describe deployment myapp-deployment
   kubectl logs <pod-name>
   ```
9. **Updated the Deployment Image**:
   ```bash
   kubectl set image deployment myapp-deployment myapp-container=nginx:1.22
   kubectl rollout status deployment myapp-deployment
   ```
10. **Rolled Back the Deployment (if needed)**:
   ```bash
   kubectl rollout undo deployment myapp-deployment
<img width="1440" alt="Screenshot 2025-04-14 at 8 17 21 PM" src="https://github.com/user-attachments/assets/62b450d5-4490-4533-ba51-8d8ff6b7b007" />
<img width="1440" alt="Screenshot 2025-04-14 at 8 17 13 PM" src="https://github.com/user-attachments/assets/658a6857-8bf2-4815-bfec-3ba8d2f637fa" />
<img width="1440" alt="Screenshot 2025-04-14 at 8 07 42 PM" src="https://github.com/user-attachments/assets/01b3960b-4a01-4293-b489-90ff593d6c63" />
<img width="1440" alt="Screenshot 2025-04-14 at 8 07 31 PM" src="https://github.com/user-attachments/assets/7846ccff-1fd2-432c-9ee9-0a2f9eff94b7" />

   ```
11. **Deleted All Resources**:
   ```bash
   kubectl delete -f deployment.yaml
   kubectl delete -f service.yaml
   kubectl delete -f configmap.yaml
   ```

## Outcome
Successfully deployed, exposed, and scaled an application on a local Minikube cluster.

## Files Included
- `deployment.yaml` – Kubernetes deployment configuration  
- `service.yaml` – Kubernetes service definition  
- `configmap.yaml` – Kubernetes ConfigMap definition  
- `README.md` – Documentation of the task
