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

## Deployment Instructions
1. Navigate to **AWS CloudFormation** in the AWS Console.
2. Click **Create Stack** and upload the provided **YAML template**.
3. Click **Next**, provide required parameters, and proceed.
4. Deploy the stack and monitor its creation progress.

## Accessing Resources
- **Web Server:** Retrieve the **Public IP** from CloudFormation Outputs and access it via a browser.
- **Private Instance:** Use **AWS SSM Session Manager** for secure CLI access.

## Cleanup
To delete all resources, delete the **CloudFormation stack** from the AWS Console.

## Notes
- The template uses **Amazon Linux 2 AMI**.
- **No SSH KeyPair** is required as SSM is used for secure access.
- Ensure your AWS account has necessary permissions before deploying.
