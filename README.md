# DevOps CI/CD Automation using Jenkins & Amazon EKS

## Project Overview
This project demonstrates an end-to-end DevOps CI/CD pipeline for deploying a Java-based web application on AWS using Jenkins, Docker, and Kubernetes (Amazon EKS).

The primary objective of this project is to implement **CI/CD automation, containerization, and cloud-based deployment**, rather than application development.

---

## Tools & Technologies
- AWS EC2, IAM, EKS
- Jenkins (CI/CD Pipeline)
- Docker & Docker Hub
- Kubernetes
- Maven & Java

---

## CI/CD Workflow
1. Source code is fetched from GitHub
2. Application is built using Maven
3. Docker image is created and pushed to Docker Hub
4. Kubernetes manifests are applied to deploy the application on Amazon EKS
5. Poll SCM is enabled to automatically trigger the pipeline on code changes

---

## Proof of Execution

### Jenkins Pipeline – Successful Build & Deployment
This screenshot shows the Jenkins pipeline executing all stages successfully, including build, Docker image creation, push, and deployment.
![Jenkins Pipeline Success](Screenshots/jenkins-pipeline-success.png)

---

### Amazon EKS Cluster Status
The EKS cluster is active and ready to host containerized applications.
![EKS Cluster Active](Screenshots/eks-cluster-active.png)

---

### Kubernetes Pods Running
This confirms that the application pods are successfully running inside the Kubernetes cluster.
![Kubernetes Pods](Screenshots/kubectl-pods.png)

---

### Kubernetes Services (NodePort)
The application is exposed using a NodePort service to allow external access.
![Kubernetes Services](Screenshots/kubectl-services.png)

---

### Application Output (Final Result)
The deployed application is accessible through the worker node’s public IP and NodePort.
![Application Output](Screenshots/application-output.png)

---

## Notes
- Application source code is not included in this repository as the focus of the project is **DevOps CI/CD automation and deployment**.
- The screenshots folder provides execution proof for each stage of the pipeline and deployment process.

---

## Author
**Sanika Kumar Patil**
