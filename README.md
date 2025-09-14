# cicd-flask-app

## Flask CI/CD on Kubernetes (Minikube)

# Overview

This project demonstrates a DevOps pipeline using:

- Dockerized Flask application
- Kubernetes Deployment & Service (NodePort)
- CI/CD pipeline with GitHub Actions (build, push to Docker Hub, deploy to K8s)
- CircleCI (optional second pipeline)

# Tech Stack

- Flask (Python)
- Docker
- Kubernetes (Minikube/EC2)
- GitHub Actions & CircleCI

---

##  Features
- Flask application containerized with Docker
- Kubernetes Deployment + Service
- NodePort service exposed at `localhost:30007`

---

##  Prerequisites
- [Docker](https://docs.docker.com/get-docker/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

---

## Deployment Steps

1. Start Minikube:
   
  -  minikube start

2. Apply Kubernetes manifests:

- kubectl apply -f k8s-deployment.yaml


3. Check pods and services:

- kubectl get pods
- kubectl get svc


4. Access the app in your browser:

http://localhost:5000

### Verify Logs

- Check logs of the Flask container:

  - kubectl logs -f <pod-name>

 # Project Structure
```
.
├── app.py                 # Flask app
├── requirements.txt       # Python dependencies
├── Dockerfile             # Docker build file
├── k8s-deployment.yaml    # Kubernetes Deployment + Service
└── README.md              # Documentation
```
# Screenshots

<img width="940" height="628" alt="image" src="https://github.com/user-attachments/assets/7e1caca8-5b93-4a88-a6a7-2be040299b01" />

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/8d20c39f-f996-4150-96b1-58581643d6f3" />

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/21f3f64d-6adc-4138-bccf-2c7f16dbf905" />

### deploye using kubernates

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/b46dc047-8139-4554-8e13-9b2de74ab046" />





