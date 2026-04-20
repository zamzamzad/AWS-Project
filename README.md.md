# AWS Enterprise Infrastructure Project

## Project Overview
This project deploys a production-ready infrastructure on AWS including VPC, EC2, ALB, and RDS.

## Architecture
- **VPC**: zmzm-vpc (10.0.0.0/16)
- **Public Subnets**: 
  - zmzm-prod-public-1 (AZ1)
  - zmzm-prod-public-2 (AZ2)
- **Private Subnets**: 
  - zmzm-prod-privet-1 (AZ1)
  - zmzm-prod-privet-2 (AZ2)
- **Internet Gateway**: Enterprise-IGW
- **Route Tables**: Public-RT, Private-RT
- **Security Groups**: ALB-SG, Web-SG, RDS-SG
- **ALB**: Enterprise-ALB (Internet-facing)
- **EC2**: 2 instances running Nginx in private subnets
- **RDS**: MySQL (designed, but not deployed due to sandbox permissions)

## Deployment
- Infrastructure deployed manually via AWS Console
- EC2 user data installs Nginx automatically

## Challenges
Due to Whiz Labs sandbox limitations, RDS creation was not permitted (rds:CreateDBCluster permission denied). The RDS security group (RDS-SG) is already configured to allow MySQL traffic only from Web-SG, and RDS would be deployed in a private subnet with public access disabled.

## Screenshots
- VPC & Subnets
- EC2 Instances (Running)
- Load Balancer (Active)
- ALB DNS name working

## Video Demo
[Insert video link here]

## GitHub Repository
[Insert your GitHub repo link here]