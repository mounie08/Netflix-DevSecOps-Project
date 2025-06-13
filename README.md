# DevSecOps Netflix Clone 🎥

A full-stack DevSecOps project to replicate a Netflix-like streaming application, built and deployed with industry-standard DevOps tools. This project demonstrates secure containerization, continuous integration/deployment, and observability using open-source solutions on AWS infrastructure.

---

## 🚀 Overview

This project is structured around the core principles of **Dev**, **Sec**, and **Ops**:

- **Dev**: Build and run the Netflix clone application locally using Docker.
- **Sec**: Integrate vulnerability scanning using **SonarQube** and **Trivy**.
- **Ops**: Automate build, test, and deployment processes using **Jenkins**, deploy to **Kubernetes** via **Helm** and **ArgoCD**, and monitor with **Prometheus** and **Grafana**.

---
## 🚀 Architecture

<div align="center">
  <img src="./public/assets/home-page.png" alt="Logo" width="100%" height="100%">
  <p align="center">Home Page</p>
</div>

This diagram illustrates the complete DevSecOps workflow implemented in this project: 
- The Netflix clone application is containerized and deployed locally on an AWS EC2 instance using Docker.

- SonarQube and Trivy are used to perform static code analysis and vulnerability scanning, enhancing application security.

- A Jenkins CI/CD pipeline automates the build process, secures the Docker image, and pushes it to Docker Hub.

- ArgoCD (a GitOps tool) continuously syncs changes from the GitHub repository into the Kubernetes cluster.

- Helm simplifies the deployment by templating Kubernetes resources for scalable and repeatable deployments.

- Prometheus collects metrics and Grafana visualizes them, enabling real-time monitoring of the deployed application and infrastructure.

The final outcome is a secure, observable, and automated deployment pipeline delivering a Netflix-style UI on Kubernetes.
## 🛠️ Tools & Technologies

| Purpose             | Tool/Technology           |
|---------------------|---------------------------|
| Containerization    | Docker                    |
| CI/CD               | Jenkins                   |
| GitOps Deployment   | ArgoCD + Helm             |
| Monitoring          | Prometheus, Grafana       |
| Security Scanning   | SonarQube, Trivy          |
| Cloud Hosting       | AWS EC2 (t2.large)        |
| API Data Source     | TMDB API                  |

---

## 🧱 Architecture Overview

1. **Application Build**:
   - Dockerfile builds the Netflix app using TMDB API for content.
   - `ARG` is used to pass the API key at runtime.
   - Docker image tagged and pushed to DockerHub.

2. **Security Integration**:
   - Run `trivy fs .` to scan file systems.
   - Use SonarQube for code quality checks.

3. **CI/CD Automation**:
   - Jenkins automates Docker builds and pushes.
   - Triggers Kubernetes deployment through ArgoCD.

4. **Kubernetes Deployment**:
   - Helm used for templated configuration.
   - ArgoCD continuously syncs with GitHub repo.

5. **Monitoring**:
   - Prometheus configured via `prometheus.yml`.
   - Grafana dashboards visualize app and node metrics.
   - Node Exporter enables host-level monitoring.

---

## 🧪 Ports Used

| Component      | Port |
|----------------|------|
| Application    | 8081 |
| Jenkins        | 8080 |
| SonarQube      | 9000 |
| Prometheus     | 9090 |

---

