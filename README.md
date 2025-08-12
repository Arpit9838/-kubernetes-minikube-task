#  Task 5: Build a Kubernetes Cluster Locally with Minikube

##  Objective
Deploy and manage a Node.js app in Kubernetes using **Minikube**.

##  Tools Used
- Minikube
- kubectl
- Docker
- Node.js App (Dockerized)

---

##  Files in this Repo
- `deployment.yaml` → Kubernetes Deployment for the app
- `service.yaml` → Kubernetes Service (NodePort) for exposing the app
- Screenshots folder → Contains output proof of all steps

---

## 📋 Steps Performed

 Install & Start Minikube

minikube start --driver=docker --memory=2500mb

 Create Deployment
bash
Copy
Edit
kubectl apply -f deployment.yaml

Expose the App as a Service
bash
Copy
Edit
kubectl apply -f service.yaml


Verify Pods
bash
Copy
Edit
kubectl get pods

Scale the Deployment
bash
Copy
Edit
kubectl scale deployment welcome-app --replicas=4
kubectl get pods

Describe Pod
bash
Copy
Edit
kubectl describe pod <pod-name>

 Access the Application
bash
Copy
Edit
minikube service welcome-service


Outcome
 Learned how to:

Start a Kubernetes cluster locally

Deploy an application using Kubernetes

Expose it using NodePort

Scale deployments

Describe pods and view logs
