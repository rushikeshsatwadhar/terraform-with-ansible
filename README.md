# 🚀 AWS Infrastructure Automation Using Terraform & Ansible

## 📖 Overview

This project demonstrates a practical Infrastructure as Code (IaC) and Configuration Management workflow by integrating Terraform and Ansible on AWS. Terraform is used to provision the required AWS infrastructure, including EC2 instances and networking resources, while Ansible automates server configuration by installing Nginx and deploying environment-specific web pages. Each environment—Development, POD, and Staging—is configured with its own customized landing page, simulating a real-world multi-environment deployment strategy. This project showcases how modern DevOps tools can be combined to deliver consistent, repeatable, and fully automated infrastructure provisioning and application deployment.

---

## 🎯 Project Workflow

```
Terraform
    │
    ▼
Provision AWS Infrastructure
    │
    ▼
EC2 Instances Created
    │
    ▼
Ansible Playbook
    │
    ▼
Install & Configure Nginx
    │
    ▼
Deploy Environment-Specific Web Pages
    │
    ▼
Development | POD | Staging
```

> 📸 **Architecture Diagram**

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/Architecture%20Diagram.png?raw=true)

---

## 🛠️ Technologies Used

- Terraform
- Ansible
- AWS EC2
- Ubuntu Linux
- Nginx
- HTML & CSS
- SSH
- Git & GitHub

---

# 📂 Project Structure

```text
terraform-meets-ansible/
│
├── terraform/
│   ├── provider.tf
│   ├── variables.tf
│   ├── main.tf
│   └── outputs.tf
│
├── ansible/
│   ├── inventory
│   ├── playbook.yml
│   └── roles/
│
├── dev/
│   └── index.html
│
├── pod/
│   └── index.html
│
├── stage/
│   └── index.html
│
└── README.md
```

---

# ⚙️ Infrastructure Provisioning

Terraform provisions the following AWS resources:

- EC2 Instances
- Security Groups
- SSH Key Pair
- Networking Configuration

📸 **Terraform Output**

*(Add screenshot here)*

---

# 🤖 Server Configuration

After the infrastructure is provisioned, Ansible automatically:

- Updates the server
- Installs Nginx
- Starts and enables the Nginx service
- Deploys custom HTML pages
- Restarts the web server

---

# 🚀 Deployment Steps

## 🔹 Step 1: Generate an SSH Key Pair

Generate an SSH key pair that Terraform and Ansible will use to authenticate with the EC2 instances.

```bash
ssh-keygen -t rsa -b 4096 -f ~/.ssh/appKey
```

---

## 🔹 Step 2: Deploy the Infrastructure

Grant execute permission to the deployment script and run it. This script provisions the AWS infrastructure using Terraform and configures the EC2 instances using Ansible.

```bash
chmod u+x deploy.sh
./deploy.sh
```

---

## 🔹 Step 3: Destroy the Infrastructure

After testing the project, remove all AWS resources to avoid unnecessary charges.

```bash
cd terraform-meets-ansible/terra-config

terraform destroy --auto-approve
```

---


📸 **Ansible Playbook Execution**

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/Ansible%20Playbook%20Execution.png?raw=true)

---

# 🌐 Environment Preview

## 🚀 Development Environment

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/Development%20Environment.png?raw=true)

---

## 📦 POD Environment

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/POD%20Environment.png?raw=true)

---

## 🎯 Staging Environment

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/Staging%20Environment.png?raw=true)

---

# 📊 AWS Resources

📸 EC2 Instances

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/EC2%20Instances.png?raw=true)

📸 Project Structure

![image alt](https://github.com/rushikeshsatwadhar/terraform-with-ansible/blob/main/Screenshot/Project%20Structure.png?raw=true)

---

# ✨ Key Features

- Infrastructure as Code (IaC)
- Automated Server Configuration
- Multi-Environment Deployment
- Nginx Web Server Automation
- Reusable Terraform Modules
- Automated Ansible Playbook Execution
- Environment-Specific Web Pages

---

# 📸 Project Gallery

- Architecture Diagram
- Terraform Apply Output
- AWS EC2 Console
- Security Group
- Ansible Playbook Output
- Development Environment
- POD Environment
- Staging Environment

---

# 📚 Learning Outcomes

- Infrastructure Provisioning with Terraform
- Configuration Management with Ansible
- AWS EC2 Automation
- Multi-Environment Deployment Strategy
- Infrastructure as Code Best Practices

---

# 👨‍💻 Author

**Rushikesh Satwadhar**

⭐ If you like this project, don't forget to **Star** the repository!
