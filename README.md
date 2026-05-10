# Secure Automated Landing Zone (Terraform)

## Project Overview

The goal is to create a secure environment with networking, a virtual machine, a database, and secure secret storage.
All deployed using code (Infrastructure as Code).

##  Architecture Summary

### The infrastructure includes:

- Custom VPC network (secure-vpc)
- Private subnet (no public access)
- Private VPC peering for Cloud SQL
- Compute Engine VM (e2-micro)
- Cloud SQL MySQL database (private IP only)
- Secret Manager for secure password storage

## Architecture Design

### Flow of the system:

1. A custom VPC network is created
2. A private subnet is attached to the VPC
3. Private Service Access (VPC peering) is configured for Cloud SQL
4. A VM instance is deployed inside the private subnet
5. A MySQL Cloud SQL instance is created with PRIVATE IP ONLY
6. Database password is stored securely in Secret Manager

 ## Security Features

- No public IP for Cloud SQL
- Private VPC access only
- Secrets stored in Google Secret Manager
- Controlled service networking using private peering

## Technologies Used
- Terraform
- Google Cloud Platform (GCP): Compute Engine, Cloud SQL (MySQL), VPC Networking, Secret Manager.
