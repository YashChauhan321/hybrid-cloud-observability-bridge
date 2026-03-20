# hybrid-cloud-observability-bridge
A Terraform-managed hybrid infrastructure monitoring stack bridging AWS EC2 and local VMware environments using Prometheus and Grafana

A DevOps project demonstrating the provisioning of hybrid infrastructure using **Terraform (IaC)** and cross-platform monitoring using **Prometheus** and **Grafana**. This project bridges a local **VMware Workstation** environment with a public cloud node in **AWS (ap-south-1)**.

## 🏗️ Architecture
- **Cloud Provider:** AWS (Mumbai Region)
- **Infrastructure as Code:** Terraform
- **Local Environment:** VMware Workstation (Ubuntu 22.04)
- **Monitoring Stack:** Prometheus, Grafana, Node Exporter
- **Containerization:** Docker & Docker Compose

## 🚀 Features
- **Automated Provisioning:** Uses Terraform to deploy EC2 instances with custom Security Groups and SSH Key Pair integration.
- **Hybrid Connectivity:** Establishes a monitoring bridge between local virtualized environments and public cloud resources.
- **Real-time Observability:** Tracks CPU, Memory, and Network metrics using Node Exporter.
- **Visualization:** Interactive Grafana dashboards for infrastructure health monitoring.

## 🛠️ Project Structure
.
├── terraform/                <-- Folder for AWS resources
│   ├── main.tf
│   ├── outputs.tf
│   ├── provider.tf
│   └── terraform.tfvars      <-- (Optional) For sensitive variables
│
├── monitoring/               <-- Folder for the Observability stack
│   ├── docker-compose.yml
│   └── prometheus.yml
│
├── .gitignore                <-- To hide .terraform and .tfstate
└── README.md                 <-- The overview I gave you

## 🚦 Current Status
- [x] Phase 1: AWS Infrastructure provisioned via Terraform.
- [x] Phase 2: Node Exporter deployed on Cloud Node.
- [/] Phase 3: Prometheus/Grafana integration (Active Development).

## 📖 How to Deploy
1. **Infrastructure:**
   ```bash
   cd terraform
   terraform init
   terraform apply
   
1. **Infrastructure:**
   ```bash
   cd monitoring
   docker-compose up -d

Author: Yash Chauhan
DevOps & Cloud Enthusiast
