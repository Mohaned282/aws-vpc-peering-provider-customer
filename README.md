# AWS VPC Peering – Provider to Customer Connectivity

## 📅 Date
July 2025

## 🛠 Tools Used
- AWS Console
- VPC Peering
- EC2 (Ubuntu)
- Route Tables
- Security Groups

## 🧭 Overview
This project demonstrates the configuration of a VPC peering connection between two VPCs (Provider and Customer) within the same AWS account. The goal is to enable secure and private communication between instances launched in each VPC.

## 🧱 Architecture
- **Provider VPC**: `10.0.0.0/16`
  - Private Subnet: `10.0.2.0/24`
- **Customer VPC**: `192.168.0.0/16`
  - Private Subnet: `192.168.2.0/24`
- **Instances**: Ubuntu EC2 instances in each private subnet
- **VPC Peering**: Connects Provider and Customer VPCs
- **Routing**: Route tables updated to allow inter-VPC traffic
- **Security Groups**: Configured to allow ICMP (ping)

## ✅ Steps Performed
1. Created two VPCs using the AWS Console
2. Created private subnets in each VPC
3. Launched Ubuntu EC2 instances in each private subnet
4. Created a VPC peering connection and accepted it
5. Updated route tables to allow traffic between the two VPCs
6. Configured Security Groups to allow ICMP traffic
7. Verified communication using ping from Provider EC2 to Customer EC2

## 🧩 Use Case
This setup simulates internal communication between isolated environments in the same AWS account. It can be applied in use cases like shared services, staging vs production environments, or logically separated application layers.
