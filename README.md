# DevOps Project: CI/CD Pipeline with CloudFormation and CodeBuild

This project demonstrates a simple but complete DevOps workflow using AWS services:

- GitHub for version control
- AWS CodePipeline for orchestration
- AWS CodeBuild for deployment
- AWS CloudFormation for infrastructure

## 📁 Repository Structure

```
.
├── app/
│   └── devops-summative.html
├── iac/
│   └── cloudformation.yaml
├── buildspec.yml
└── README.md
```

## 🔄 Pipeline Flow

1. Push code to GitHub triggers CodePipeline
2. CodeBuild runs `buildspec.yml`, deploying the HTML app to EC2
3. CloudFormation creates/updates the environment (EC2, SG, etc.)

## ✅ Benefits
- Single repository, single pipeline
- Fully automated deployment
- Uses AWS Free Tier efficiently
- Demonstrates GitOps + Infrastructure as Code

## ⚠️ Notes
- Ensure EC2 instance is stopped when not in use to avoid charges
- Replace placeholders in `buildspec.yml` with your actual EC2 DNS and key
