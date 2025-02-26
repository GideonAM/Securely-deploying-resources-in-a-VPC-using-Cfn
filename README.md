# Securely Deploying Resources in a VPC using CloudFormation

## Overview
This CloudFormation template provisions a secure Virtual Private Cloud (VPC) with public and private subnets, along with necessary networking components. It also deploys an Apache web server on a public EC2 instance and a private EC2 instance with AWS Systems Manager (SSM) Session Manager enabled.

## Resources Created
- **VPC** with a public and private subnet
- **Internet Gateway** for external access
- **NAT Gateway** for private instance internet access
- **Route Tables** for public and private traffic routing
- **Security Groups** to control access
- **IAM Role** for SSM access
- **EC2 Instances**
    - **Public instance:** Apache web server with auto-start
    - **Private instance:** SSM-enabled for secure management
