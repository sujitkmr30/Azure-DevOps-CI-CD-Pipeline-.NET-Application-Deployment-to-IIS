# Azure DevOps CI/CD Pipeline – .NET Application Deployment to IIS

## 📌 Project Overview
This project demonstrates an end-to-end CI/CD pipeline using **Azure DevOps** to build, test, and deploy a **.NET 7 web application** to **IIS** using a **self-hosted Windows agent**.

The pipeline automatically performs:

- Source code checkout
- Application build
- Unit testing
- Artifact publishing
- Deployment to IIS

- ## 🏗 CI/CD Architecture

Developer → Git Repository → Azure DevOps Pipeline  
↓  
CI Stage  
- Restore Packages  
- Build Application  
- Run Tests  
- Publish Artifacts  

↓  

CD Stage  
- Download Artifacts  
- Deploy to IIS Server  
- Restart Application Pool

## ⚙ Technologies Used

- .NET 7
- Azure DevOps
- Azure Pipelines (YAML)
- IIS (Internet Information Services)
- PowerShell
- Git

## 🚀 Pipeline Stages
### 1️⃣ Continuous Integration (CI)

The CI stage performs:

- Install .NET SDK
- Restore NuGet packages
- Build the application
- Run unit tests
- Publish build artifacts

### 2️⃣ Continuous Deployment (CD)

The CD stage performs:

- Download build artifacts
- Copy application files to IIS directory
- Create IIS website if not exists
- Restart IIS Application Pool

## 📄 Azure Pipeline Configuration

The pipeline configuration is defined in:
azure-pipelines.yml
It contains two stages:

- CI – Build & Test
- CD – Deploy to IIS

## 🌐 Deployment Details

| Parameter | Value |
|----------|------|
| IIS Site Name | SampleApp |
| Deployment Path | C:\inetpub\wwwroot\SampleApp |
| Port | 8080 |
| Agent Pool | azure-devops-iis-cicd |

## ▶ How to Run the Pipeline

1. Push code to **main branch**
2. Azure DevOps pipeline triggers automatically
3. CI stage builds and tests the application
4. CD stage deploys application to IIS

## 📂 Project Structure
project-root
│
├── SampleApp
│   └── SampleApp.csproj
│
├── azure-pipelines.yml
│
└── README.md

## 👨‍💻 Author

**Sujit Kumar Bauri**

DevOps Engineer  
GitHub: https://github.com/sujitkmr30

![Azure DevOps](https://img.shields.io/badge/Azure%20DevOps-CI/CD-blue)
![.NET](https://img.shields.io/badge/.NET-7-purple)
![IIS](https://img.shields.io/badge/IIS-Deployment-green)

## 🌐 Access Application    