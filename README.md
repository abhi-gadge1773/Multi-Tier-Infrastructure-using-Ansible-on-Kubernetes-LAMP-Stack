# 🌐 Multi-Tier Infrastructure using Ansible on Kubernetes (LAMP Stack)

This project demonstrates how to automate the deployment of a **Multi-Tier LAMP Stack Application** using **Ansible** and **Kubernetes**. It provisions a robust web architecture consisting of **Apache, MySQL**, and **PHP** containers orchestrated by **K8s**, all configured automatically with Ansible Playbooks.

---

## 📌 Project Overview

| Component | Description |
|----------|-------------|
| **Infrastructure** | Multi-Tier (Frontend + Backend + Database) |
| **Orchestration Tool** | Kubernetes |
| **Automation Tool** | Ansible |
| **Tech Stack** | Apache (Frontend), PHP (App), MySQL (DB) |
| **Platform** | Docker, K8s, Ansible, Linux |
| **Use Case** | Scalable web application deployment with infrastructure automation |

---

## 🏗️ Architecture
Client
│
▼
[Apache - PHP] <-- Frontend Pod (Apache + PHP)
│
▼
[MySQL DB] <-- Backend Pod (MySQL)


Each tier is deployed on a Kubernetes Pod and managed using Ansible Playbooks for seamless configuration and orchestration.

---

## 🚀 Features

- 🔄 Infrastructure automation using Ansible
- 📦 LAMP stack deployment on Kubernetes
- 🐳 Dockerized application components
- 🧩 Modular and scalable architecture
- 🔍 Logs and access verification using `kubectl`
- 🔐 Secure MySQL password provisioning using Ansible Vault (optional)

---

## 📂 Project Structure
├── ansible/
│ ├── inventory
│ ├── playbook.yml
│ ├── apache_deploy.yml
│ ├── mysql_deploy.yml
│ └── php_deploy.yml
├── k8s-manifests/
│ ├── apache-deployment.yaml
│ ├── php-deployment.yaml
│ └── mysql-deployment.yaml
├── Dockerfiles/
│ ├── apache/
│ └── php/
└── README.md


---

## ⚙️ Prerequisites

- Docker & Docker Compose
- Kubernetes (Minikube, Kind, or Cluster)
- Ansible (v2.9+)
- kubectl CLI

---

## 📦 Setup Instructions

### 🔧 1. Clone the repository

```bash
git clone https://github.com/abhi-gadge1773/Multi-Tier-Infrastructure-using-Ansible-on-Kubernetes-LAMP-Stack.git
cd Multi-Tier-Infrastructure-using-Ansible-on-Kubernetes-LAMP-Stack
```


⚙️ 2. Configure Ansible Inventory
Edit the ansible/inventory file to match your local/remote setup.

🚀 3. Run Ansible Playbook
```
cd ansible
ansible-playbook -i inventory playbook.yml
```
This will deploy Apache, PHP, and MySQL services on Kubernetes using the respective deployment manifests.

🧪 Verification
Check all running pods
```
kubectl get pods
```

Access frontend service
Use the minikube service command or check the NodePort to access the Apache/PHP web interfac
```
minikube service apache-service

```
🙋‍♂️ Author

Abhijeet Gadge

GitHub | LinkedIn | Twitter
