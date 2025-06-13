# IRCTC Migration on AWS – Architecture Design

## Project Overview
This project outlines a high-level architecture design for migrating the Indian Railway Catering and Tourism Corporation (IRCTC) platform from on-premise infrastructure to AWS Cloud. The project focuses on scalability, reliability, cost optimization, and secure infrastructure setup using AWS services such as EC2, RDS, Lambda, Route 53, CloudWatch, and more.  
I worked on this as part of my AWS Cloud Internship at F13 Technologies, in collaboration with my team.

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


