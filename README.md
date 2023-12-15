# Dynamic-Web-Application-on-AWS
Project One: Host a Dynamic Ecommerce Website on AWS

# Cloud-Based Web Application Infrastructure

## Description

This project outlines the architecture for a highly available and scalable web application hosted on AWS. It leverages several AWS services to ensure fault tolerance, security, and performance.

## Architecture

The architecture is a 3-tier setup with a VPC configured for public and private subnets across multiple availability zones. Key components include:

- **EC2 Instances**: Hosts the web application in an Auto Scaling group.
- **RDS Instances**: MySQL database with a master-slave setup for high availability.
- **S3 Buckets**: Stores application code and assets.
- **Application Load Balancer (ALB)**: Distributes incoming traffic.
- **Route 53**: Manages DNS records.
- **IAM Roles and Policies**: Manage permissions and security.
- **SNS**: Handles notification services.
- **Certificate Manager**: Manages SSL/TLS certificates.

## Requirements

- AWS Account
- Domain Name (for Route 53 setup)
- AWS CLI and configured AWS credentials

## Installation

1. Set up VPC with public and private subnets.
2. Launch EC2 instances with an AMI that has the web application.
3. Configure RDS instances for the database tier.
4. Set up the ALB to distribute traffic to the EC2 instances.
5. Create an S3 bucket for code deployment and static assets.
6. Configure Route 53 for domain name management.
7. Assign necessary IAM roles and policies.
8. Configure SNS for notifications.
9. Request and manage SSL/TLS certificates through the Certificate Manager.
10. Import your SQL data into RDS using MySQL Workbench.

## Usage

To deploy the web application:

1. Push the code to the S3 bucket.
2. Update the Auto Scaling group to pull the latest code from S3.
3. Access the application via the domain configured in Route 53.

