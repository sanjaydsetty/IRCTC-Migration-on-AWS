# IRCTC Migration on AWS – Architecture Design

## Project Overview
This project was designed as part of our AWS Cloud Internship at F13 Technologies. It focuses on migrating the Indian Railway Catering and Tourism Corporation (IRCTC) platform to the AWS Cloud, improving performance, scalability, and cost-efficiency.

The migration aims to enhance:
- System reliability
- Performance during peak usage (like Tatkal bookings)
- Disaster recovery capabilities
- Cost efficiency and scalability

---

## System Overview

### Current Infrastructure
- Hosted in traditional data centers
- Issues with scalability, performance under load, and maintenance

### AWS Cloud Setup
- Web servers hosted in EC2 with Load Balancer
- RDS for backend databases in private subnet
- AWS Lambda for dynamic operations
- Route 53, CloudWatch, SNS, and IAM for routing, monitoring, notifications, and security

---

## Architecture Diagram

![Architecture](Architecture_Diagram/irctc_architecture.png)

---

## Scalability, Reliability & Cost Optimization

- **Auto Scaling Group** with ALB ensures performance and resilience
- **RDS Read Replicas** handle high read-loads efficiently
- **CloudWatch & Alarms** enable responsive scaling
- **Lifecycle policies and S3** reduce storage cost

---

## Security & Routing

- **Route 53 + ALB** for DNS and traffic distribution
- **Security Groups** limit database access
- **Two-step user verification** through SEC-MAN + OTP
- **VPC** with public/private subnet separation
- **NAT Gateway** allows secure outbound traffic for backend

---

## Monitoring & Logs

- **CloudWatch**: For real-time system monitoring
- **CloudTrail**: API logging for compliance and auditing
- **Kinesis + Firehose**: Real-time streaming data ingestion
- **Athena**: Serverless querying over logs and S3 data

---

## 📄 Full Report

Find the complete report in [`docs/IRS_on_AWS_Report.pdf`](docs/IRS_on_AWS_Report.pdf)

---


