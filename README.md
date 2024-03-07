Overview
This repository contains the source code and configuration files for automating the Continuous Integration and Continuous Deployment (CI/CD) pipeline of deploying an application image onto an Amazon Elastic Kubernetes Service (EKS) cluster. The pipeline includes provisioning the necessary infrastructure, setting up Jenkins for automation, integrating various tools for code analysis and security scanning, and deploying Docker images onto the EKS cluster.

Technologies Used
    Infrastructure as Code: Terraform
    Automation Server: Jenkins
    Containerization: Docker
    Orchestration: Kubernetes (Amazon EKS)
    Package Management: Helm
    Programming Language: Java
    Version Control: Git
    Build Tool: Maven
    Container Orchestration Tool: Kubectl
    Code Analysis: SonarQube
    Security Scanning: OWASP Dependency-Check, Trivy
    Monitoring: Prometheus

CI/CD Pipeline Overview
Infrastructure Provisioning
Utilized Terraform to provision the Virtual Private Cloud (VPC) for the EKS cluster.
EKS Cluster Configuration
Created a modularized Terraform configuration for setting up the EKS cluster.
Jenkins Shell Script Setup
Configured a Jenkins shell script for installing and configuring the necessary tools and dependencies, including Java, Git, Maven, Jenkins, Terraform, Kubectl, Docker, and Helm.
Integrations
Integrated SonarQube for code analysis, OWASP Dependency-Check for identifying known vulnerabilities in dependencies, and Trivy for container image scanning.
Jenkins Setup
Configured Jenkins and installed essential plugins such as Docker, Kubernetes, SonarQube, OWASP Dependency-Check, Trivy, and Prometheus Metrics.
ECR Image Repository Creation
Set up an Elastic Container Registry (ECR) repository to store Docker images.
EC2 Instance Modification
Modified the EC2 instance to communicate with the ECR repository by adjusting the IAM role.
Jenkins Pipeline Setup
Created a new pipeline item in Jenkins and configured build triggers using GitHub webhooks and SCM polling.
Usage
Clone this repository.
Ensure Jenkins, Docker, and Kubernetes are properly configured.
Set up the required IAM roles for communication with ECR.
Configure Jenkins with the necessary plugins and integrate SonarQube, OWASP Dependency-Check, and Trivy.
Create a new pipeline item in Jenkins and configure the build triggers.
Reference the Jenkinsfile path for pipeline execution.
Contributors
Your Name or Organization
License
This project is licensed under the MIT License - see the LICENSE file for details.