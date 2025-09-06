# 🚀 AWS Services Overview

This document provides a categorized list of **AWS services** with short descriptions of **why we should use them**.

---

## 1. Compute Services

| Service | Why Use It |
|---------|------------|
| **EC2 (Elastic Compute Cloud)** | Run virtual machines in the cloud with full control over OS, networking, and storage. |
| **Lambda** | Serverless compute – run code without managing servers, pay only for execution time. |
| **ECS (Elastic Container Service)** | Orchestrate Docker containers easily on AWS-managed infrastructure. |
| **EKS (Elastic Kubernetes Service)** | Run Kubernetes without managing the control plane, integrate with AWS services. |
| **Lightsail** | Simple VMs for small apps, websites, and quick prototyping. |
| **Batch** | Run batch computing jobs at scale with automatic resource provisioning. |
| **Outposts** | Bring AWS infrastructure on-premises for hybrid cloud. |
| **Local Zones** | Extend AWS services close to end-users for low-latency apps. |

---

## 2. Storage Services

| Service | Why Use It |
|---------|------------|
| **S3 (Simple Storage Service)** | Object storage for files, images, backups – durable and highly scalable. |
| **EBS (Elastic Block Store)** | Block storage for EC2 instances, persistent disks. |
| **EFS (Elastic File System)** | Fully managed, scalable shared file system for multiple EC2 instances. |
| **FSx** | Managed Windows File Server and Lustre for HPC workloads. |
| **Glacier (S3 Glacier)** | Low-cost, long-term archival storage. |
| **Storage Gateway** | Connect on-premises systems to AWS cloud storage seamlessly. |

---

## 3. Database Services

| Service | Why Use It |
|---------|------------|
| **RDS** | Managed relational databases (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, Aurora). |
| **Aurora** | High-performance, MySQL/Postgres-compatible cloud database. |
| **DynamoDB** | Fully managed NoSQL database with millisecond response times. |
| **ElastiCache** | Managed Redis/Memcached for caching and real-time performance. |
| **Neptune** | Graph database for relationships and connected data. |
| **Redshift** | Data warehouse for analytics at scale. |
| **DocumentDB** | MongoDB-compatible managed NoSQL database. |
| **Timestream** | Time-series database for IoT, monitoring, analytics. |

---

## 4. Networking & Content Delivery

| Service | Why Use It |
|---------|------------|
| **VPC (Virtual Private Cloud)** | Isolated network environment with subnets, routing, and firewalls. |
| **Route 53** | Scalable DNS and domain registration service. |
| **CloudFront** | CDN for caching and distributing content globally with low latency. |
| **API Gateway** | Manage, secure, and scale APIs. |
| **Direct Connect** | Dedicated network link from on-premises to AWS. |
| **Global Accelerator** | Improves availability and performance of apps with static IPs. |
| **PrivateLink** | Secure private connectivity between VPCs and services. |

---

## 5. Security, Identity & Compliance

| Service | Why Use It |
|---------|------------|
| **IAM** | Control access with users, roles, and policies. |
| **Cognito** | User authentication, sign-in, and federation for apps. |
| **Secrets Manager** | Securely store and rotate credentials, API keys, and secrets. |
| **KMS** | Create and control encryption keys. |
| **Shield** | Managed DDoS protection. |
| **WAF (Web Application Firewall)** | Protect apps from common web exploits. |
| **Inspector** | Automated security assessment service. |
| **GuardDuty** | Threat detection and monitoring service. |
| **Macie** | Detect sensitive data (like PII) in S3 using ML. |

---

## 6. Analytics & Big Data

| Service | Why Use It |
|---------|------------|
| **Athena** | Query S3 data using SQL (serverless). |
| **EMR** | Big data processing with Hadoop, Spark, Hive. |
| **Kinesis** | Real-time streaming data processing. |
| **QuickSight** | Business intelligence and dashboards. |
| **Data Pipeline** | Move and process data between services. |
| **Glue** | ETL (Extract, Transform, Load) for preparing datasets. |

---

## 7. Machine Learning & AI

| Service | Why Use It |
|---------|------------|
| **SageMaker** | Build, train, and deploy ML models at scale. |
| **Rekognition** | Image and video analysis (faces, objects, moderation). |
| **Polly** | Text-to-speech with natural voices. |
| **Lex** | Build chatbots and conversational interfaces. |
| **Comprehend** | NLP for text analysis (sentiment, entities, language). |
| **Translate** | Language translation. |
| **Forecast** | Time-series forecasting using ML. |
| **Textract** | Extract text and data from scanned documents. |

---

## 8. Developer Tools

| Service | Why Use It |
|---------|------------|
| **CodeCommit** | Managed Git repositories. |
| **CodeBuild** | Build and test code in the cloud. |
| **CodeDeploy** | Automate deployments to EC2, Lambda, on-prem servers. |
| **CodePipeline** | CI/CD pipeline automation. |
| **Cloud9** | Web-based IDE. |
| **X-Ray** | Debug and analyze distributed applications. |

---

## 9. Management & Monitoring

| Service | Why Use It |
|---------|------------|
| **CloudWatch** | Monitor logs, metrics, and events across AWS resources. |
| **CloudTrail** | Track API calls and user activity for compliance and auditing. |
| **Config** | Track AWS resource configurations over time. |
| **Trusted Advisor** | Cost optimization, performance, and security recommendations. |
| **Systems Manager (SSM)** | Manage servers and automation tasks at scale. |
| **Service Catalog** | Manage approved IT service catalogs. |

---

## 10. Migration & Transfer

| Service | Why Use It |
|---------|------------|
| **DMS** | Migrate databases with minimal downtime. |
| **SMS** | Migrate on-premises servers to AWS. |
| **Snowball** | Transfer large datasets physically (petabyte-scale). |
| **Migration Hub** | Track and manage migrations across AWS services. |
| **DataSync** | Automate large data transfers between on-prem and AWS. |

---

✅ This list covers the **core AWS services** grouped by category for quick reference.
```

---















# aws-notes


    pricing by instance :
    ----------------------
    2cpu+1gb ram: $4 per months for 2GB its $8 and for 4GB its will be $16
    https://aws.amazon.com/ec2/pricing/on-demand/
    
    amazon ec2 default user:
    --------------------------
    
    normally , if you choose ubuntu image default user will be ubuntu
    if you choose Amazon linux image default user will be ec2-user ...etc
    you can connect via connect buttion of ec2 /you can see default user name aswell here.
    
    
  default user list 
  --------------------------------------
        
        Amazon Linux 2023: ec2-user
        Amazon Linux 2: ec2-user
        Amazon Linux: ec2-user
        CentOS:	centos or ec2-user
        Debian:	admin
        Fedora:	fedora or ec2-user
        RHEL:	ec2-user or root
        SUSE:	ec2-user or root
        Ubuntu:	ubuntu
        Oracle:	ec2-user
        Bitnami:	bitnami
        Other:	Check with the AMI provider

        reference:
        https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connection-prereqs.html



