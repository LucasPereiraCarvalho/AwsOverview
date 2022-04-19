# Aws overview <!-- omit in toc -->

## Contents <!-- omit in toc -->

- [1. Traditionally, how to build infrastructure](#1-traditionally-how-to-build-infrastructure)
  - [1.1. How websites work](#11-how-websites-work)
  - [1.2. What is a server composed of?](#12-what-is-a-server-composed-of)
  - [1.3. IT Terminology](#13-it-terminology)
  - [1.4. Problems with traditional IT approach](#14-problems-with-traditional-it-approach)
- [2. What is Cloud Computing?](#2-what-is-cloud-computing)
  - [2.1. You've been using some Cloud services](#21-youve-been-using-some-cloud-services)
  - [2.2. The Deployment Models of the Cloud](#22-the-deployment-models-of-the-cloud)
    - [2.2.1. Private Cloud:](#221-private-cloud)
    - [2.2.2. Public Cloud:](#222-public-cloud)
    - [2.2.3. Hybrid Cloud:](#223-hybrid-cloud)
  - [2.3. The Five Characteristics of Cloud Computing](#23-the-five-characteristics-of-cloud-computing)
  - [2.4. Six Advantages of Cloud Computing](#24-six-advantages-of-cloud-computing)
  - [2.5. Problems solved by the Cloud](#25-problems-solved-by-the-cloud)
  - [2.6. Types of Cloud Computing](#26-types-of-cloud-computing)
  - [2.7. Example of Cloud Computing Types](#27-example-of-cloud-computing-types)
  - [2.8. Pricing of the Cloud - Quick Overview](#28-pricing-of-the-cloud---quick-overview)
  - [2.9. AWS Global Infrastructure](#29-aws-global-infrastructure)
  - [2.10. AWS Regions](#210-aws-regions)
  - [2.11. How to choose an AWS Region?](#211-how-to-choose-an-aws-region)
  - [2.12. AWS Availability Zones](#212-aws-availability-zones)
  - [2.13. AWS Points of Presence (Edge Locations)](#213-aws-points-of-presence-edge-locations)
  - [2.14. Tour of the AWS Console](#214-tour-of-the-aws-console)
  - [2.15. Shared Responsibility Model diagram](#215-shared-responsibility-model-diagram)
  - [2.16. AWS Acceptable Use Policy](#216-aws-acceptable-use-policy)
- [3. IAM - Identity and Access Management](#3-iam---identity-and-access-management)
  - [3.1. IAM: Users & Groups](#31-iam-users--groups)
  - [3.2. IAM: Permissions](#32-iam-permissions)
  - [3.3. IAM: Policies Structure](#33-iam-policies-structure)
  - [3.4. IAM - Password Policy](#34-iam---password-policy)
  - [3.5. Multi Factor Authentication - MFA](#35-multi-factor-authentication---mfa)
  - [3.6. MFA devices options in AWS](#36-mfa-devices-options-in-aws)
  - [3.7. How can users access AWS ?](#37-how-can-users-access-aws-)
  - [3.8. What's the AWS CLI?](#38-whats-the-aws-cli)
  - [3.9. What's the AWS SDK?](#39-whats-the-aws-sdk)
  - [3.10. IAM Roles for Services](#310-iam-roles-for-services)
  - [3.11. IAM Security Tools](#311-iam-security-tools)
  - [3.12. IAM Guidelines & Best Practices](#312-iam-guidelines--best-practices)
  - [3.13. Shared Responsibility Model for IAM](#313-shared-responsibility-model-for-iam)
  - [3.14. IAM - Summary](#314-iam---summary)
- [4. EC2 - Elastic Compute Cloud](#4-ec2---elastic-compute-cloud)
  - [4.1. Amazon EC2](#41-amazon-ec2)
  - [4.2. EC2 sizing & configuration options](#42-ec2-sizing--configuration-options)
  - [4.3. EC2 User Data](#43-ec2-user-data)
  - [4.4. EC2 Instance Types - Overview](#44-ec2-instance-types---overview)
  - [4.5. EC2 Instance Types](#45-ec2-instance-types)
    - [4.5.1. General Purpose](#451-general-purpose)
    - [4.5.2. Compute Optimized](#452-compute-optimized)
    - [4.5.3. Memory Optimized](#453-memory-optimized)
    - [4.5.4. Storage Optimized](#454-storage-optimized)
  - [4.6. EC2 Instance Types: example](#46-ec2-instance-types-example)
  - [4.7. Introduction to Security Groups](#47-introduction-to-security-groups)
  - [4.8. Security Groups Deeper Dive](#48-security-groups-deeper-dive)
  - [4.9. Security Groups Good to know](#49-security-groups-good-to-know)
  - [4.10. Classic Ports to know](#410-classic-ports-to-know)
  - [4.11. How to SSH into your EC2 Instance](#411-how-to-ssh-into-your-ec2-instance)
  - [4.12. EC2 Instance Connect](#412-ec2-instance-connect)
  - [4.13. EC2 Instances Purchasing Options](#413-ec2-instances-purchasing-options)
    - [4.13.1. EC2 On Demand](#4131-ec2-on-demand)
    - [4.13.2. EC2 Reserved Instances](#4132-ec2-reserved-instances)
    - [4.13.3. EC2 Spot Instances](#4133-ec2-spot-instances)
    - [4.13.4. EC2 Dedicated Hosts](#4134-ec2-dedicated-hosts)
    - [4.13.5. EC2 Dedicated Instances](#4135-ec2-dedicated-instances)
  - [4.14. Which purchasing option is right for me? (correlation with Hotel)](#414-which-purchasing-option-is-right-for-me-correlation-with-hotel)
  - [4.15. Shared Responsibility Model for EC2](#415-shared-responsibility-model-for-ec2)
  - [4.16. EC2 - Summary](#416-ec2---summary)
- [5. EC2 Instance Storage](#5-ec2-instance-storage)
  - [5.1. What's an EBS Volume?](#51-whats-an-ebs-volume)
  - [5.2. EBS Volume](#52-ebs-volume)
  - [5.3. EBS - Delete on Termination attribute](#53-ebs---delete-on-termination-attribute)
  - [5.4. EBS Snapshots](#54-ebs-snapshots)
  - [5.5. AMI Overview](#55-ami-overview)
  - [5.6. AMI Process (from an EC2 instance)](#56-ami-process-from-an-ec2-instance)
  - [5.7. EC2 Image Builder](#57-ec2-image-builder)
  - [5.8. EC2 Instance Store](#58-ec2-instance-store)
  - [5.9. EFS - Elastic File System](#59-efs---elastic-file-system)
  - [5.10. EFS Infrequent Access (EFS-IA)](#510-efs-infrequent-access-efs-ia)
  - [5.11. Shared Responsibility Model for EC2 Storage](#511-shared-responsibility-model-for-ec2-storage)
  - [5.12. Amazon FSx - Overview](#512-amazon-fsx---overview)
    - [5.12.1. Amazon FSx for Windows File Server](#5121-amazon-fsx-for-windows-file-server)
    - [5.12.2. Amazon FSx for Lustre](#5122-amazon-fsx-for-lustre)
  - [5.13. EC2 Instance Storage Summary](#513-ec2-instance-storage-summary)
- [6. Elastic Load Balancing & Auto Scaling Groups](#6-elastic-load-balancing--auto-scaling-groups)
  - [6.1. Scalability & High Availability](#61-scalability--high-availability)
    - [6.1.1. Vertical Scalability](#611-vertical-scalability)
    - [6.1.2. Horizontal Scalability](#612-horizontal-scalability)
  - [6.2. High Availability](#62-high-availability)
  - [6.3. High Availability & Scalability For EC2](#63-high-availability--scalability-for-ec2)
  - [6.4. Scalability vs Elasticity (vs Agility)](#64-scalability-vs-elasticity-vs-agility)
  - [6.5. What is load balancing?](#65-what-is-load-balancing)
  - [6.6. Why use a load balancer?](#66-why-use-a-load-balancer)
  - [6.7. Why use an Elastic Load Balancer (ELB)?](#67-why-use-an-elastic-load-balancer-elb)
  - [6.8. What's an Auto Scaling Group?](#68-whats-an-auto-scaling-group)
  - [6.9. Auto Scaling Groups - Scaling Strategies](#69-auto-scaling-groups---scaling-strategies)
  - [6.10. ELB & ASG - Summary](#610-elb--asg---summary)
- [7. Amazon S3](#7-amazon-s3)
  - [7.1. Introduction](#71-introduction)
  - [7.2. S3 Use cases](#72-s3-use-cases)
  - [7.3. Amazon S3 Overview](#73-amazon-s3-overview)
    - [7.3.1. Buckets](#731-buckets)
    - [7.3.2. Objects](#732-objects)
  - [7.4. S3 Security](#74-s3-security)
    - [7.4.1. S3 Bucket Policies](#741-s3-bucket-policies)
    - [7.4.2. Bucket settings for Block Public Access](#742-bucket-settings-for-block-public-access)
  - [7.5. S3 Websites](#75-s3-websites)
  - [7.6. Amazon S3 - Versioning](#76-amazon-s3---versioning)
  - [7.7. S3 Access Logs](#77-s3-access-logs)
  - [7.8. S3 Replication (CRR & SRR)](#78-s3-replication-crr--srr)
  - [7.9. S3 Storage Classes](#79-s3-storage-classes)
  - [7.10. S3 Durability and Availability](#710-s3-durability-and-availability)
  - [7.11. S3 Standard - General Purposes](#711-s3-standard---general-purposes)
  - [7.12. S3 Standard - Infrequent Access (IA)](#712-s3-standard---infrequent-access-ia)
  - [7.13. S3 Intelligent-Tiering](#713-s3-intelligent-tiering)
  - [7.14. S3 One Zone - Infrequent Access (IA)](#714-s3-one-zone---infrequent-access-ia)
  - [7.15. Amazon Glacier & Glacier Deep Archive](#715-amazon-glacier--glacier-deep-archive)
  - [7.16. S3 Storage Classes Comparison](#716-s3-storage-classes-comparison)
  - [7.17. Moving between storage classes](#717-moving-between-storage-classes)
  - [7.18. S3 Object Lock & Glacier Vault Lock](#718-s3-object-lock--glacier-vault-lock)
  - [7.19. S3 Encryption](#719-s3-encryption)
  - [7.20. Shared Responsibility Model for S3](#720-shared-responsibility-model-for-s3)
  - [7.21. AWS Snow Family](#721-aws-snow-family)
  - [7.22. Data Migrations with AWS Snow Family](#722-data-migrations-with-aws-snow-family)
    - [7.22.1. AWS Snowcone](#7221-aws-snowcone)
    - [7.22.2. Snowball Edge (for data transfers)](#7222-snowball-edge-for-data-transfers)
    - [7.22.3. AWS Snowmobile](#7223-aws-snowmobile)
  - [7.23. Snow Family - Usage Process](#723-snow-family---usage-process)
  - [7.24. What is Edge Computing?](#724-what-is-edge-computing)
  - [7.25. Snow Family - Edge Computing](#725-snow-family---edge-computing)
  - [7.26. AWS OpsHub](#726-aws-opshub)
  - [7.27. Hybrid Cloud for Storage](#727-hybrid-cloud-for-storage)
  - [7.28. AWS Storage Gateway](#728-aws-storage-gateway)
  - [7.29. Amazon S3 - Summary](#729-amazon-s3---summary)
- [8. Databases](#8-databases)
  - [8.1. Introduction](#81-introduction)
  - [8.2. Relational Databases](#82-relational-databases)
  - [8.3. NoSQL Databases](#83-nosql-databases)
  - [8.4. NoSQL data example: JSON](#84-nosql-data-example-json)
  - [8.5. Databases & Shared Responsibility on AWS](#85-databases--shared-responsibility-on-aws)
  - [8.6. AWS RDS Overview](#86-aws-rds-overview)
  - [8.7. Advantage over using RDS versus deploying DB on EC2](#87-advantage-over-using-rds-versus-deploying-db-on-ec2)
  - [8.8. Amazon Aurora](#88-amazon-aurora)
  - [8.9. RDS Deployments: Read Replicas, Multi-AZ, Multi-Region](#89-rds-deployments-read-replicas-multi-az-multi-region)
    - [8.9.1. Read Replicas](#891-read-replicas)
    - [8.9.2. Multi-AZ](#892-multi-az)
    - [8.9.3. Multi-Region](#893-multi-region)
    - [8.9.4. Resume](#894-resume)
  - [8.10. Amazon ElastiCache Overview](#810-amazon-elasticache-overview)
  - [8.11. DynamoDB](#811-dynamodb)
    - [8.11.1. DynamoDB Accelerator - DAX](#8111-dynamodb-accelerator---dax)
    - [8.11.2. DynamoDB - Global Tables](#8112-dynamodb---global-tables)
  - [8.12. Redshift Overview](#812-redshift-overview)
  - [8.13. Amazon EMR](#813-amazon-emr)
  - [8.14. Amazon Athena](#814-amazon-athena)
  - [8.15. Amazon QuickSight](#815-amazon-quicksight)
  - [8.16. DocumentDB](#816-documentdb)
  - [8.17. Amazon Neptune](#817-amazon-neptune)
  - [8.18. Amazon QLDB](#818-amazon-qldb)
  - [8.19. Amazon Managed Blockchain](#819-amazon-managed-blockchain)
  - [8.20. AWS Glue](#820-aws-glue)
  - [8.21. DMS - Database Migration Service](#821-dms---database-migration-service)
  - [8.22. Databases & Analytics Summary in AWS](#822-databases--analytics-summary-in-aws)
- [9. Other Compute Services: ECS, Lambda, Batch, Lightsail](#9-other-compute-services-ecs-lambda-batch-lightsail)
  - [9.1. ECS](#91-ecs)
  - [9.2. Fargate](#92-fargate)
  - [9.3. ECR](#93-ecr)
  - [9.4. What's serverless?](#94-whats-serverless)
  - [9.5. Why AWS Lambda?](#95-why-aws-lambda)
    - [9.5.1. Benefits of AWS Lambda](#951-benefits-of-aws-lambda)
    - [9.5.2. AWS Lambda language support](#952-aws-lambda-language-support)
    - [9.5.3. AWS Lambda Pricing: example](#953-aws-lambda-pricing-example)
  - [9.6. Amazon API Gateway](#96-amazon-api-gateway)
  - [9.7. AWS Batch](#97-aws-batch)
  - [9.8. Batch vs Lambda](#98-batch-vs-lambda)
  - [9.9. Amazon Lightsail](#99-amazon-lightsail)
  - [9.10. Other Compute - Summary](#910-other-compute---summary)
  - [9.11. Lambda Summary](#911-lambda-summary)
- [10. Deploying and Managing Infrastructure at Scale](#10-deploying-and-managing-infrastructure-at-scale)
  - [10.1. What is CloudFormation?](#101-what-is-cloudformation)
    - [10.1.1. Benefits of AWS CloudFormation](#1011-benefits-of-aws-cloudformation)
    - [10.1.2. CloudFormation Stack Designer](#1012-cloudformation-stack-designer)
  - [10.2. AWS Cloud Development Kit (CDK)](#102-aws-cloud-development-kit-cdk)
  - [10.3. Developer problems on AWS](#103-developer-problems-on-aws)
  - [10.4. AWS Elastic Beanstalk Overview](#104-aws-elastic-beanstalk-overview)
  - [10.5. Elastic Beanstalk](#105-elastic-beanstalk)
    - [10.5.1. Health Monitoring](#1051-health-monitoring)
  - [10.6. AWS CodeDeploy](#106-aws-codedeploy)
  - [10.7. AWS CodeCommit](#107-aws-codecommit)
  - [10.8. AWS CodeBuild](#108-aws-codebuild)
  - [10.9. AWS CodePipeline](#109-aws-codepipeline)
  - [10.10. AWS CodeArtifact](#1010-aws-codeartifact)
  - [10.11. AWS CodeStar](#1011-aws-codestar)
  - [10.12. AWS Cloud9](#1012-aws-cloud9)
  - [10.13. AWS Systems Manager (SSM)](#1013-aws-systems-manager-ssm)
    - [10.13.1. How Systems Manager works?](#10131-how-systems-manager-works)
    - [10.13.2. Systems Manager - SSM Session Manager](#10132-systems-manager---ssm-session-manager)
  - [10.14. AWS OpsWorks](#1014-aws-opsworks)
  - [10.15. Deployment - Summary](#1015-deployment---summary)
- [11. Global Infrastructure](#11-global-infrastructure)
  - [11.1. Why make a global application?](#111-why-make-a-global-application)
  - [11.2. Global AWS Infrastructure](#112-global-aws-infrastructure)
  - [11.3. Global Applications in AWS](#113-global-applications-in-aws)
  - [11.4. Amazon Route 53 Overview](#114-amazon-route-53-overview)
    - [11.4.1. Route 53 policies](#1141-route-53-policies)
  - [11.5. AWS CloudFront](#115-aws-cloudfront)
  - [11.6. CloudFront - Origins](#116-cloudfront---origins)
  - [11.7. CloudFront vs S3 Cross Region Replication](#117-cloudfront-vs-s3-cross-region-replication)
  - [11.8. S3 Transfer Acceleration](#118-s3-transfer-acceleration)
  - [11.9. AWS Global Accelerator](#119-aws-global-accelerator)
  - [11.10. AWS Global Accelerator vs CloudFront](#1110-aws-global-accelerator-vs-cloudfront)
  - [11.11. AWS Outposts](#1111-aws-outposts)
  - [11.12. AWS WaveLength](#1112-aws-wavelength)
  - [11.13. AWS Local Zones](#1113-aws-local-zones)
  - [11.14. Global Applications Architecture](#1114-global-applications-architecture)
  - [11.15. Global Applications in AWS - Summary](#1115-global-applications-in-aws---summary)
  - [11.16. Global Applications in AWS - Summary](#1116-global-applications-in-aws---summary)
- [12. Cloud Integration](#12-cloud-integration)
  - [12.1. Amazon SQS - Standard Queue](#121-amazon-sqs---standard-queue)
  - [12.2. Amazon Kinesis](#122-amazon-kinesis)
  - [12.3. Amazon SNS](#123-amazon-sns)
  - [12.4. Amazon MQ](#124-amazon-mq)
  - [12.5. Integration - Summary](#125-integration---summary)
- [13. Cloud Monitoring](#13-cloud-monitoring)
  - [13.1. Amazon CloudWatch Metrics](#131-amazon-cloudwatch-metrics)
    - [13.1.1. Important Metrics](#1311-important-metrics)
  - [13.2. Amazon CloudWatch Alarms](#132-amazon-cloudwatch-alarms)
  - [13.3. Amazon CloudWatch Logs](#133-amazon-cloudwatch-logs)
  - [13.4. CloudWatch Logs for EC2](#134-cloudwatch-logs-for-ec2)
  - [13.5. Amazon CloudWatch Events](#135-amazon-cloudwatch-events)
  - [13.6. Amazon EventBridge](#136-amazon-eventbridge)
  - [13.7. AWS CloudTrail](#137-aws-cloudtrail)
  - [13.8. CloudTrail Events](#138-cloudtrail-events)
    - [13.8.1. CloudTrail Insights Events](#1381-cloudtrail-insights-events)
    - [13.8.2. CloudTrail Events Retention](#1382-cloudtrail-events-retention)
  - [13.9. AWS X-Ray](#139-aws-x-ray)
    - [13.9.1. AWS X-Ray advantages](#1391-aws-x-ray-advantages)
  - [13.10. Amazon CodeGuru](#1310-amazon-codeguru)
  - [13.11. Amazon CodeGuru Reviewer](#1311-amazon-codeguru-reviewer)
    - [13.11.1. Amazon CodeGuru Profiler](#13111-amazon-codeguru-profiler)
  - [13.12. AWS Status - Service Health Dashboard](#1312-aws-status---service-health-dashboard)
  - [13.13. AWS Personal Health Dashboard](#1313-aws-personal-health-dashboard)
  - [13.14. Monitoring Summary](#1314-monitoring-summary)
- [14. VPC](#14-vpc)
  - [14.1. VPC - Crash Course](#141-vpc---crash-course)
  - [14.2. VPC & Subnets Primer](#142-vpc--subnets-primer)
  - [14.3. Internet Gateway & NAT Gateways](#143-internet-gateway--nat-gateways)
  - [14.4. Network ACL & Security Groups](#144-network-acl--security-groups)
  - [14.5. Network ACLs vs Security Groups](#145-network-acls-vs-security-groups)
  - [14.6. VPC Flow Logs](#146-vpc-flow-logs)
  - [14.7. VPC Peering](#147-vpc-peering)
  - [14.8. VPC Endpoints](#148-vpc-endpoints)
  - [14.9. Site to Site VPN & Direct Connect](#149-site-to-site-vpn--direct-connect)
  - [14.10. Site-to-Site VPN](#1410-site-to-site-vpn)
  - [14.11. Transit Gateway](#1411-transit-gateway)
  - [14.12. VPC Closing Comments](#1412-vpc-closing-comments)
- [15. Security & Compliance](#15-security--compliance)
  - [15.1. AWS Shared Responsibility Model](#151-aws-shared-responsibility-model)
    - [15.1.1. Example, for RDS](#1511-example-for-rds)
    - [15.1.2. Example, for S3](#1512-example-for-s3)
  - [15.2. DDOS Protection on AWS](#152-ddos-protection-on-aws)
  - [15.3. AWS Shield](#153-aws-shield)
  - [15.4. AWS WAF - Web Application Firewall](#154-aws-waf---web-application-firewall)
  - [15.5. Penetration Testing on AWS Cloud](#155-penetration-testing-on-aws-cloud)
  - [15.6. Data at rest vs. Data in transit](#156-data-at-rest-vs-data-in-transit)
  - [15.7. AWS KMS (Key Management Service)](#157-aws-kms-key-management-service)
  - [15.8. CloudHSM](#158-cloudhsm)
  - [15.9. Types of CMK (Customer Master Keys)](#159-types-of-cmk-customer-master-keys)
  - [15.10. AWS Certificate Manager (ACM)](#1510-aws-certificate-manager-acm)
  - [15.11. AWS Secrets Manager](#1511-aws-secrets-manager)
  - [15.12. AWS Artifact (not really a service)](#1512-aws-artifact-not-really-a-service)
  - [15.13. Amazon GuardDuty](#1513-amazon-guardduty)
  - [15.14. Amazon Inspector](#1514-amazon-inspector)
    - [15.14.1. What does AWS Inspector evaluate?](#15141-what-does-aws-inspector-evaluate)
  - [15.15. AWS Config](#1515-aws-config)
  - [15.16. Amazon Macie](#1516-amazon-macie)
  - [15.17. AWS Security Hub](#1517-aws-security-hub)
  - [15.18. Amazon Detective](#1518-amazon-detective)
  - [15.19. AWS Abuse](#1519-aws-abuse)
  - [15.20. Root user privileges](#1520-root-user-privileges)
  - [15.21. Summary: Security & Compliance](#1521-summary-security--compliance)
- [16. Machine Learning](#16-machine-learning)
  - [16.1. Amazon Rekognition](#161-amazon-rekognition)
  - [16.2. Amazon Transcribe](#162-amazon-transcribe)
  - [16.3. Amazon Polly](#163-amazon-polly)
  - [16.4. Amazon Translate](#164-amazon-translate)
  - [16.5. Amazon Lex & Connect](#165-amazon-lex--connect)
  - [16.6. Amazon Comprehend](#166-amazon-comprehend)
  - [16.7. Amazon SageMaker](#167-amazon-sagemaker)
  - [16.8. Amazon Forecast](#168-amazon-forecast)
  - [16.9. Amazon Kendra](#169-amazon-kendra)
  - [16.10. Amazon Personalize](#1610-amazon-personalize)
  - [16.11. AWS Machine Learning - Summary](#1611-aws-machine-learning---summary)
- [17. Advanced Identity](#17-advanced-identity)
  - [17.1. AWS STS (SecurityToken Service)](#171-aws-sts-securitytoken-service)
  - [17.2. Amazon Cognito](#172-amazon-cognito)
  - [17.3. What is Microsoft Active Directory (AD)?](#173-what-is-microsoft-active-directory-ad)
    - [17.3.1. AWS Directory Services](#1731-aws-directory-services)
  - [17.4. AWS Organizations](#174-aws-organizations)
  - [17.5. AWS Single Sign-On (SSO)](#175-aws-single-sign-on-sso)
  - [17.6. Advanced Identity - Summary](#176-advanced-identity---summary)
- [18. Other AWS Services](#18-other-aws-services)
  - [18.1. Amazon WorkSpaces](#181-amazon-workspaces)
  - [18.2. Amazon AppStream 2.0](#182-amazon-appstream-20)
    - [18.2.1. Amazon AppStream 2.0 vs WorkSpaces](#1821-amazon-appstream-20-vs-workspaces)
  - [18.3. Amazon Sumerian](#183-amazon-sumerian)
  - [18.4. AWS IoT Core](#184-aws-iot-core)
  - [18.5. Amazon Elastic Transcoder](#185-amazon-elastic-transcoder)
  - [18.6. AWS Device Farm](#186-aws-device-farm)
  - [18.7. AWS Backup](#187-aws-backup)
    - [18.7.1. Disaster Recovery Strategies](#1871-disaster-recovery-strategies)
  - [18.8. AWS Elastic Disaster Recovery (DRS)](#188-aws-elastic-disaster-recovery-drs)
  - [18.9. AWS DataSync](#189-aws-datasync)
  - [18.10. AWS Fault Injection Simulator (FIS)](#1810-aws-fault-injection-simulator-fis)
- [19. AWS related Abbreviations & Acronyms](#19-aws-related-abbreviations--acronyms)
  - [19.1. A](#191-a)
  - [19.2. B](#192-b)
  - [19.3. C](#193-c)
  - [19.4. D](#194-d)
  - [19.5. E](#195-e)
  - [19.6. F](#196-f)
  - [19.7. H](#197-h)
  - [19.8. I](#198-i)
  - [19.9. J](#199-j)
  - [19.10. K](#1910-k)
  - [19.11. L](#1911-l)
  - [19.12. M](#1912-m)
  - [19.13. N](#1913-n)
  - [19.14. O](#1914-o)
  - [19.15. P](#1915-p)
  - [19.16. Q](#1916-q)
  - [19.17. R](#1917-r)
  - [19.18. S](#1918-s)
  - [19.19. T](#1919-t)
  - [19.20. V](#1920-v)
  - [19.21. W](#1921-w)
- [20. Commands](#20-commands)

## 1. Traditionally, how to build infrastructure

### 1.1. How websites work

- Clients have IP addresses.
- Servers have IP addresses.

### 1.2. What is a server composed of?

- Compute: CPU.
- Memory: RAM.
- Storage: Data.
- Database: Store data in a structured way.
- Network: Routers, switch, DNS server.

### 1.3. IT Terminology

- Network: cables, routers and servers connected with each other.
- Router: A networking device that forwards data packets between computer
  networks. They know where to send your packets on the internet!
- Switch: Takes a packet and send it to the correct server / client on your network.

### 1.4. Problems with traditional IT approach

- Pay for the rent for the data center.
- Pay for power supply, cooling, maintenance.
- Adding and replacing hardware takes time.
- Scaling is limited.
- Hire 24/7 team to monitor the infrastructure.
- How to deal with disasters? (earthquake, power shutdown, fire...).
- Can we externalize all this? **CLOUD**

## 2. What is Cloud Computing?

- Cloud computing is the on-demand delivery of compute power, database storage, applications, and other IT resources.
- Through a cloud services platform with pay-as-you-go pricing.
- You can provision exactly the right type and size of computing resources you need.
- You can access as many resources as you need, almost instantly.
- Simple way to access servers, storage, databases and a set of application services.
- Amazon Web Services owns and maintains the network-connected hardware required for these application services, while you provision and use what you need via a web application.

### 2.1. You've been using some Cloud services

- Gmail
  - E-mail cloud service
  - Pay for ONLY your emails stored (no infrastructure, etc.)
- Dropbox
  - Cloud Storage Service
  - Originally built on AWS
- Netflix
  - Built on AWS
  - Video on Demand

### 2.2. The Deployment Models of the Cloud

#### 2.2.1. Private Cloud:

- Cloud services used by a single organization, not exposed to the public.
- Complete control.
- Security for sensitive applications.
- Meet specific business needs.

#### 2.2.2. Public Cloud:

- Cloud resources owned and operated by a third-party cloud service provider delivered over the Internet.

#### 2.2.3. Hybrid Cloud:

- Keep some servers on premises and extend some capabilities to the Cloud.
- Control over sensitive assets in your private infrastructure.
- Flexibility and cost-effectiveness of the public cloud.

### 2.3. The Five Characteristics of Cloud Computing

- On-demand self service:
  - Users can provision resources and use them without human interaction from the service provider
- Broad network access:
  - Resources available over the network, and can be accessed by diverse client platforms
- Multi-tenancy and resource pooling:
  - Multiple customers can share the same infrastructure and applications with security and privacy
  - Multiple customers are serviced from the same physical resources
- Rapid elasticity and scalability:
  - Automatically and quickly acquire and dispose resources when needed
  - Quickly and easily scale based on demand
- Measured service:
  - Usage is measured, users pay correctly for what they have used

### 2.4. Six Advantages of Cloud Computing

- Trade capital expense (CAPEX) for operational expense (OPEX)
  - Pay On-Demand: don't own hardware
  - Reduced Total Cost of Ownership (TCO) & Operational Expense (OPEX)
- Benefit from massive economies of scale
  - Prices are reduced as AWS is more efficient due to large scale
- Stop guessing capacity
  - Scale based on actual measured usage
- Increase speed and agility
- Stop spending money running and maintaining data centers
- Go global in minutes: leverage the AWS global infrastructure

### 2.5. Problems solved by the Cloud

- Flexibility: change resource types when needed
- Cost-Effectiveness: pay as you go, for what you use
- Scalability: accommodate larger loads by making hardware stronger or adding additional nodes
- Elasticity: ability to scale out and scale-in when needed
- High-availability and fault-tolerance: build across data centers
- Agility: rapidly develop, test and launch software applications

### 2.6. Types of Cloud Computing

- Infrastructure as a Service (IaaS)
  - Provide building blocks for cloud IT.
  - Provides networking, computers, data storage space.
  - Highest level of flexibility.
  - Easy parallel with traditional on-premises IT.
- Platform as a Service (PaaS)
  - Removes the need for your organization to manage the underlying infrastructure.
  - Focus on the deployment and management of your applications.
- Software as a Service (SaaS)
  - Completed product that is run and managed by the service provider.

### 2.7. Example of Cloud Computing Types

- Infrastructure as a Service
  - Amazon EC2 (on AWS)
  - GCP, Azure, Rackspace, Digital Ocean, Linode
- Platform as a Service:
  - Elastic Beanstalk (on AWS)
  - Heroku, Google App Engine (GCP), Windows Azure (Microsoft)
- Software as a Service:
  - Many AWS services (ex: Rekognition for Machine Learning)
  - Google Apps (Gmail), Dropbox, Zoom

### 2.8. Pricing of the Cloud - Quick Overview

- AWS has 3 pricing fundamentals, following the pay-as-you-go pricing
  model
  - Compute:
    - Pay for compute time
  - Storage:
    - Pay for data stored in the Cloud
  - Data transfer **OUT** of the Cloud:
    - Data transfer IN is free
  - Solves the expensive issue of traditional IT

### 2.9. AWS Global Infrastructure

- AWS Regions.
- AWS Availability Zones.
- AWS Data Centers.
- AWS Edge Locations / Points of Presence.
- https://infrastructure.aws/

### 2.10. AWS Regions

- AWS has Regions all around the world.
- Names can be us-east-1, eu-west-3...
- A region is a cluster of data centers.
- Most AWS services are region-scoped.

### 2.11. How to choose an AWS Region?

- **Compliance** with data governance and legal requirements: data never leaves a region without your explicit permission.
- **Proximity** to customers: reduced latency.
- **Available** services within a Region: new services and new features aren't available in every Region.
- **Pricing**: pricing varies region to region and is transparent in the service pricing page.
- **Capacity is unlimited in the cloud, you do not need to worry about it. The 4 points of considerations when choosing an AWS Region are: compliance with data governance and legal requirements, proximity to customers, available services and features within a Region, and pricing.**

### 2.12. AWS Availability Zones

- Each region has many availability zones (usually 3, min is 2, max is 6). Example:
  - ap-southeast-2a
  - ap-southeast-2b
  - ap-southeast-2c
- Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity.
- They're separate from each other, so that they're isolated from disasters.
- They're connected with high bandwidth, ultra-low latency networking.

### 2.13. AWS Points of Presence (Edge Locations)

- Amazon has 216 Points of Presence (205 Edge Locations & 11 Regional Caches) in 84 cities across 42 countries.
- Content is delivered to end users with lower latency.

### 2.14. Tour of the AWS Console

- AWS has Global Services:
  - Identity and Access Management (IAM)
  - Route 53 (DNS service)
  - CloudFront (Content Delivery Network)
  - WAF (Web Application Firewall)
- Most AWS services are Region-scoped:
  - Amazon EC2 (Infrastructure as a Service)
  - Elastic Beanstalk (Platform as a Service)
  - Lambda (Function as a Service)
  - Rekognition (Software as a Service)
- Region Table: https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services

### 2.15. Shared Responsibility Model diagram

- AWS = RESPONSIBILITY FOR THE SECURITY OF THE CLOUD
- CUSTOMER = RESPONSIBILITY FOR THE SECURITY IN THE CLOUD
- https://aws.amazon.com/compliance/shared-responsibility-model/

### 2.16. AWS Acceptable Use Policy

- https://aws.amazon.com/aup/
- No Illegal, Harmful, or Offensive Use or Content
- No Security Violations
- No Network Abuse
- No E-Mail or Other Message Abuse

## 3. IAM - Identity and Access Management

### 3.1. IAM: Users & Groups

- IAM = Identity and Access Management, **Global service**.
- **Root account** created by default, shouldn't be used or shared.
- **Users** are people within your organization, and can be grouped.
- **Groups** only contain users, not other groups.
- Users don't have to belong to a group, and user can belong to multiple groups.

### 3.2. IAM: Permissions

- **Users or Groups** can be assigned JSON documents called policies.
- These policies define the **permissions** of the users.
- In AWS you apply the **least privilege** principle: don't give more permissions than a user needs.

### 3.3. IAM: Policies Structure

- Consists of:
  - **Version**: policy language version, always include "YYYY-MM-DD".
  - **Id**: an identifier for the policy (optional).
  - **Statement**: one or more individual statements (required).
- Statements consists of:
  - **Sid**: an identifier for the statement (optional).
  - **Effect**: whether the statement allows or denies access (Allow, Deny).
  - **Principal**: account/user/role to which this policy applied to.
  - **Action**: list of actions this policy allows or denies.
  - **Resource**: list of resources to which the actions applied to.
  - **Condition**: conditions for when this policy is in effect (optional).

### 3.4. IAM - Password Policy

- Strong passwords = higher security for your account.
- In AWS, you can setup a password policy:
  - Set a minimum password length.
  - Require specific character types:
    - Including uppercase letters.
    - Lowercase letters.
    - Numbers.
    - Non-alphanumeric characters.
- Allow all IAM users to change their own passwords.
- Require users to change their password after some time (password expiration).
- Prevent password re-use.

### 3.5. Multi Factor Authentication - MFA

- Users have access to your account and can possibly change configurations or delete resources in your AWS account
- **You want to protect your Root Accounts and IAM users**
- MFA = password you know + security device you own
- Main benefit of MFA:
  - If a password is stolen or hacked, the account is not compromised

### 3.6. MFA devices options in AWS

- Virtual MFA device:
  - Google AuthenLcator (phone only).
  - Authy (multi-device).
  - Support for multiple tokens on a single device.
- Universal 2nd Factor (U2F) Security Key:
  - YubiKey by Yubico (3rd party)
    - Support for multiple tokens on a single device. Support for multiple root and IAM users using a single security key
- Hardware Key Fob MFA Device:
  - Provided by Gemalto (3rd party)
- Hardware Key Fob MFA Device for AWS GovCloud (US):
  - Provided by SurePassID (3rd party)

### 3.7. How can users access AWS ?

- To access AWS, you have three options:
  - AWS Management Console (protected by password + MFA).
  - AWS Command Line Interface (CLI): protected by access keys.
  - AWS Software Developer Kit (SDK) - for code: protected by access keys.
- Access Keys are generated through the AWS Console.
- Users manage their own access keys.
- Access Keys are secret, just like a password. Don't share them.
- Access Key ID ~= username.
- Secret Access Key ~= password.
- Example (Fake) Access Keys.
  - Access key ID: AKIASK4E37PV4983d6C.
  - Secret Access Key: AZPN3zojWozWCndIjhB0Unh8239a1bzbzO5fqqkZq.
  - **Remember: don't share your access keys.**

### 3.8. What's the AWS CLI?

- A tool that enables you to interact with AWS services using commands in your command-line shell
- Direct access to the public APIs of AWS services
- You can develop scripts to manage your resources
- It's open-source https://github.com/aws/aws-cli
- Alternative to using AWS Management Console

### 3.9. What's the AWS SDK?

- AWS Software Development Kit (AWS SDK)
- Language-specific APIs (set of libraries)
- Enables you to access and manage AWS services programmatically
- Embedded within your application
- Supports:
  - SDKs (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++, C#)
  - Mobile SDKs (Android, iOS, ...)
  - IoT Device SDKs (Embedded C, Arduino, ...)
- Example: AWS CLI is built on AWS SDK for Python

### 3.10. IAM Roles for Services

- Some AWS service will need to perform actions on your behalf.
- To do so, we will assign permissions to AWS services with IAM Roles.
- Common roles:
  - EC2 Instance Roles.
  - Lambda Function Roles.
  - Roles for CloudFormation.

### 3.11. IAM Security Tools

- IAM Credentials Report (account-level)
  - A report that lists all your account's users and the status of their various credentials
- IAM Access Advisor (user-level)
  - Access advisor shows the service permissions granted to a user and when those services were last accessed.
  - You can use this information to revise your policies.

### 3.12. IAM Guidelines & Best Practices

- Don't use the root account except for AWS account setup
- One physical user = One AWS user
- **Assign users to groups** and assign permissions to groups
- Create a **strong password policy**
- Use and enforce the use of **Multi Factor Authentication (MFA)**
- Create and use **Roles** for giving permissions to AWS services
- Use Access Keys for Programmatic Access (CLI / SDK)
- Audit permissions of your account with the IAM Credentials Report
- **Never share IAM users & Access Keys**

### 3.13. Shared Responsibility Model for IAM

- AWS:
  - Infrastructure (global network security)
  - Configuration and vulnerability analysis
  - Compliance validation
- You (Customer):
  - Users, Groups, Roles, Policies management and monitoring
  - Enable MFA on all accounts
  - Rotate all your keys often
  - Use IAM tools to apply appropriate permissions
  - Analyze access patterns & review permissions

### 3.14. IAM - Summary

- **Users**: mapped to a physical user, has a password for AWS Console
- **Groups**: contains users only
- **Policies**: JSON document that outlines permissions for users or groups
- **Roles**: for EC2 instances or AWS services
- **Security**: MFA + Password Policy
- **AWS CLI**: manage your AWS services using the command-line
- **AWS SDK**: manage your AWS services using a programming language
- **Access Keys**: access AWS using the CLI or SDK
- **Audit**: IAM Credential Reports & IAM Access Advisor

## 4. EC2 - Elastic Compute Cloud

### 4.1. Amazon EC2

- EC2 is one of the most popular of AWS' offering.
- EC2 = Elastic Compute Cloud = Infrastructure as a Service.
- It mainly consists in the capability of:
  - Renting virtual machines (EC2).
  - Storing data on virtual drives (EBS).
  - Distributing load across machines (ELB).
  - Scaling the services using an auto-scaling group (ASG).
- Knowing EC2 is fundamental to understand how the Cloud works.

### 4.2. EC2 sizing & configuration options

- Operating System (OS): Linux, Windows or Mac OS.
- How much compute power & cores (CPU).
- How much random-access memory (RAM).
- How much storage space:
  - Network-attached (EBS & EFS).
  - hardware (EC2 Instance Store).
- Network card: speed of the card, Public IP address.
- Firewall rules: security group.
- Bootstrap script (configure at first launch): EC2 User Data.

### 4.3. EC2 User Data

- It is possible to bootstrap our instances using an EC2 User data script.
- **bootstrapping** means launching commands when a machine starts.
- That script is **only run once** at the instance first start.
- EC2 user data is used to automate boot tasks such as:
  - Installing updates.
  - Installing software.
  - Downloading common files from the internet.
  - Anything you can think of.
- The EC2 User Data Script runs with the root user.

### 4.4. EC2 Instance Types - Overview

- You can use different types of EC2 instances that are optimised for different use cases (https://aws.amazon.com/ec2/instance-types/).
- AWS has the following naming convention:
  - m5.2xlarge
    - m: instance class
    - 5: generation (AWS improves them over time)
    - 2xlarge: size within the instance class

### 4.5. EC2 Instance Types

#### 4.5.1. General Purpose

- Great for a diversity of workloads such as web servers or code repositories.
- Balance between:
  - Compute.
  - Memory.
  - Networking.
- In the course, we will be using the t2.micro which is a General Purpose EC2 instance.

#### 4.5.2. Compute Optimized

- Great for compute-intensive tasks that require high performance processors:
  - Batch processing workloads.
  - Media transcoding.
  - High performance web servers.
  - High performance computing (HPC).
  - Scientific modeling & machine learning.
  - Dedicated gaming servers.

#### 4.5.3. Memory Optimized

- Fast performance for workloads that process large data sets in memory
- Use cases:
- High performance, relational/non-relational databases
- Distributed web scale cache stores
- In-memory databases optimized for BI (business intelligence)
- Applications performing real-time processing of big unstructured data

#### 4.5.4. Storage Optimized

- Great for storage-intensive tasks that require high, sequential read and write
  access to large data sets on local storage
- Use cases:
- High frequency online transaction processing (OLTP) systems
- Relational & NoSQL databases
- Cache for in-memory databases (for example, Redis)
- Data warehousing applications
- Distributed file systems

### 4.6. EC2 Instance Types: example

| Instance    | vCPU | Mem (GiB) | Storage          | Network performance | EBS Banwidth () |
| ----------- | ---- | --------- | ---------------- | ------------------- | --------------- |
| t2.micro    | 1    | 1         | EBS-Only         | Low to Moderate     |                 |
| t2.xlarge   | 4    | 16        | EBS-Only         | Moderate            |                 |
| c5d.4xlarge | 16   | 32        | 1 x 400 NVMe SSD | Up to 10 Gbps       | 4,750           |
| r5.16xlarge | 64   | 512       | EBS-Only         | 20 Gbps             | 13,600          |
| m5.8xlarge  | 32   | 128       | EBS-Only         | 10 Gbps             | 6,800           |

- t2.micro is part of the AWS free tier (up to 750 hours per month)

### 4.7. Introduction to Security Groups

- Security Groups are the fundamental of network security in AWS
- They control how traffic is allowed into or out of our EC2 Instances.
- Security groups only contain **allow** rules
- Security groups rules can reference by IP or by security group

### 4.8. Security Groups Deeper Dive

- Security groups are acting as a "firewall" on EC2 instances
- They regulate:
  - Access to Ports
  - Authorised IP ranges IPv4 and IPv6
  - Control of inbound network (from other to the instance)
  - Control of outbound network (from the instance to other)

### 4.9. Security Groups Good to know

- Can be attached to multiple instances
- Locked down to a region / VPC combination
- Does live "outside" the EC2 - if traffic is blocked the EC2 instance won't see it
- It's good to maintain one separate security group for SSH access
- If your application is not accessible (time out), then it's a security group issue
- If your application gives a "connection refused" error, then it's an application error or it's not launched
- All inbound traffic is **blocked** by default
- All outbound traffic is **authorised** by default

### 4.10. Classic Ports to know

- 22 = SSH (Secure Shell) - log into a Linux instance
- 21 = FTP (File Transfer Protocol) - upload files into a file share
- 22 = SFTP (Secure File Transfer Protocol) - upload files using SSH
- 80 = HTTP - access unsecured websites
- 443 = HTTPS - access secured websites
- 3389 = RDP (Remote Desktop Protocol) - log into a Windows instance

### 4.11. How to SSH into your EC2 Instance

- Windows
- We'll learn how to SSH into your EC2 instance using Windows
- Configure pem file
  ![Permission Propertie Aws PemFile](/Images/PermissionPropertieAwsPemFile.png)
- Command
  - ssh -i D:\MY_PENFILE.pem ec2-user@PUBLIC_IP

### 4.12. EC2 Instance Connect

- Connect to your EC2 instance within your browser
- No need to use your key file that was downloaded
- The "magic" is that a temporary key is uploaded onto EC2 by AWS
- **Works only out-of-the-box with Amazon Linux 2**
- Need to make sure the port 22 is still opened!

### 4.13. EC2 Instances Purchasing Options

- On-Demand Instances: short workload, predictable pricing
- Reserved: (MINIMUM 1 year)
  - Reserved Instances: long workloads
  - Convertible Reserved Instances: long workloads with flexible instances
  - Scheduled Reserved Instances: example - every Thursday between 3 and 6 pm
- Spot Instances: short workloads, cheap, can lose instances (less reliable)
- Dedicated Hosts: book an entire physical server, control instance placement
- Dedicated Instances: no other customers will share your hardware

#### 4.13.1. EC2 On Demand

- Pay for what you use:
  - Linux or Windows - billing per second, after the first minute
  - All other operating systems - billing per hour
- Has the highest cost but no upfront payment
- No long-term commitment
- Recommended for **short-term** and **un-interrupted workloads**, where you can't predict how the application will behave

#### 4.13.2. EC2 Reserved Instances

- Up to 72% discount compared to On-demand
- Reservation period: 1 year = + discount | 3 years = +++ discount
- Purchasing options: no upfront | partial upfront = + | All upfront = ++ discount
- Reserve a specific instance type
- Recommended for steady-state usage applications (think database)
- Convertible Reserved Instance
  - Can change the EC2 instance type
  - Up to 45% discount
- Scheduled Reserved Instances
  - Launch within time window you reserve
  - When you require a fraction of day / week / month
  - Commitment for 1 year only

#### 4.13.3. EC2 Spot Instances

- Can get a discount of up to 90% compared to On-demand
- Instances that you can "lose" at any point of time if your max price is less than the
  current spot price
- The MOST cost-efficient instances in AWS
- Useful for workloads that are resilient to failure
  - Batch jobs
  - Data analysis
  - Image processing
  - Any distributed workloads
  - Workloads with a flexible start and end time
- Not suitable for critical jobs or databases

#### 4.13.4. EC2 Dedicated Hosts

- An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use. Dedicated Hosts can help you address compliance requirements and reduce costs by allowing you to use your existing server-bound software licenses.
- Allocated for your account for a 3-year period reservation
- More expensive
- Useful for software that have complicated licensing model (BYOL - Bring Your Own License)
- Or for companies that have strong regulatory or compliance needs

#### 4.13.5. EC2 Dedicated Instances

- Instances running on hardware that's dedicated to you
- May share hardware with other instances in same account
- No control over instance placement (can move hardware after Stop / Start)

### 4.14. Which purchasing option is right for me? (correlation with Hotel)

- On demand: coming and staying in resort whenever we like, we pay the full price
- Reserved: like planning ahead and if we plan to stay for a long time, we may get a good discount.
- Spot instances: the hotel allows people to bid for the empty rooms and the highest bidder keeps the rooms. You can get kicked out at any time
- Dedicated Hosts: We book an entire building of the resort

### 4.15. Shared Responsibility Model for EC2

- AWS:
  - Infrastructure (global network security)
  - Isolation on physical hosts
  - Replacing faulty hardware
  - Compliance validation
- You:
  - Security Groups rules
  - Operating-system patches and updates
  - Software and utilities installed on the EC2 instance
  - IAM Roles assigned to EC2ASDASD\_\_& IAM user access management
  - Data security on your instance

### 4.16. EC2 - Summary

- EC2 Instance: AMI (OS) + Instance Size (CPU + RAM) + Storage + security groups + EC2 User Data.
- Security Groups: Firewall attached to the EC2 instance.
- EC2 User Data: Script launched at the first start of an instance.
- SSH: start a terminal into our EC2 Instances (port 22).
- EC2 Instance Role: link to IAM roles.
- Purchasing Options: On-Demand, Spot, Reserved (Standard + Convertible + Scheduled), Dedicated Host, Dedicated Instance.

## 5. EC2 Instance Storage

### 5.1. What's an EBS Volume?

- An **EBS (Elastic Block Store) Volume** is a **network drive** you can attach to your instances while they run.
- It allows your instances to persist data, even after their termination.
- **They can only be mounted to one instance at a time (at the CCP level)**.
- They are bound to a specific **availability zone (AZ)**.
- Analogy: Think of them as a "network USB stick".

### 5.2. EBS Volume

- It's a network drive (i.e. not a physical drive).
  - It uses the network to communicate the instance, which means there might be a bit of latency.
  - It can be detached from an EC2 instance and attached to another one quickly.
- It's locked to an Availability Zone (AZ).
  - An EBS Volume in us-east-1a cannot be attached to us-east-1b.
  - To move a volume across, you first need to **snapshot** it.
- Have a provisioned capacity (size in GBs, and IOPS).
  - You get billed for all the provisioned capacity.
  - You can increase the capacity of the drive over time.

### 5.3. EBS - Delete on Termination attribute

- Controls the EBS behaviour when an EC2 instance terminates
  - By default, the root EBS volume is deleted (attribute enabled)
  - By default, any other attached EBS volume is not deleted (attribute disabled)
- This can be controlled by the AWS console / AWS CLI
- **Use case: preserve root volume when instance is terminated**

### 5.4. EBS Snapshots

- Make a backup (snapshot) of your EBS volume at a point in time.
- Not necessary to detach volume to do snapshot, **but recommended**.
- Can copy snapshots across AZ or Region.

### 5.5. AMI Overview

- AMI = Amazon Machine Image.
- AMI are a **customization** of an EC2 instance.
  - You add your own software, configuration, operating system, monitoring...
  - Faster boot / configuration time because all your software is pre-packaged
- AMI are built for a **specific region** (and can be copied across regions).
- You can launch EC2 instances from:
  - A Public AMI: AWS provided
  - Your own AMI: you make and maintain them yourself
  - An AWS Marketplace AMI: an AMI someone else made (and potentially sells)

### 5.6. AMI Process (from an EC2 instance)

- Start an EC2 instance and customize it.
- Stop the instance (for data integrity).
- Build an AMI - this will also create EBS snapshots.
- Launch instances from other AMIs.

### 5.7. EC2 Image Builder

- Used to automate the creation of Virtual Machines or container images.
- => Automate the creation, maintain, validate and test **EC2 AMIs**.
- Can be run on a schedule (weekly, whenever packages are updated, etc...).
- Free service (only pay for the underlying resources).
- Steps:
  1. EC2 Image Builder
     1. Create
  2. Builder EC2 Instance
     1. Create
  3. New AMI
  4. Test EC2 Instance

### 5.8. EC2 Instance Store

- EBS volumes are **network drives** with good but "limited" performance.
- **If you need a high-performance hardware disk, use EC2 Instance Store**.
- Better I/O performance.
- EC2 Instance Store lose their storage if they're stopped (ephemeral).
- Good for buffer / cache / scratch data / temporary content.
- Risk of data loss if hardware fails.
- Backups and Replication are your responsibility.

### 5.9. EFS - Elastic File System

- Managed NFS (network file system) that **can be mounted on 100s of EC2**.
- EFS works with **Linux** EC2 instances in **multi-AZ**.
- Highly available, scalable, expensive (3x gp2), pay per use, no capacity planning.

### 5.10. EFS Infrequent Access (EFS-IA)

- **Storage class** that is cost-optimized for files not accessed every day.
- Up to 92% lower cost compared to EFS Standard.
- EFS will automatically move your files to EFS-IA based on the last time they were accessed.
- Enable EFS-IA with a Lifecycle Policy.
- Example: move files that are not accessed for 60 days to EFS-IA.
- Transparent to the applications accessing EFS.

### 5.11. Shared Responsibility Model for EC2 Storage

- AWS
  - Infrastructure.
  - Replication for data for EBS volumes & EFS drives.
  - Replacing faulty hardware.
  - Ensuring their employees cannot access your data.
- You
  - Setting up backup / snapshot procedures.
  - Setting up data encryption.
  - Responsibility of any data on the drives.
  - Understanding the risk of using EC2 Instance Store.

### 5.12. Amazon FSx - Overview

- Launch 3rd party high-performance file systems on AWS.
- Fully managed service.
- Products:
  - FSx for Lustre
  - FSx for Windows File Server
  - FSx for NetApp ONTAP

#### 5.12.1. Amazon FSx for Windows File Server

- A fully managed, highly reliable, and scalable Windows native shared file system.
- Built on Windows File Server.
- Supports SMB protocol & Windows NTFS.
- Integrated with Microsoft Active Directory.
- Can be accessed from AWS or your on-premise infrastructure.

#### 5.12.2. Amazon FSx for Lustre

- A fully managed, high-performance, scalable file storage for **High Performance Computing (HPC)**.
- The name Lustre is derived from "Linux" and "cluster".
- Machine Learning, Analytics, Video Processing, Financial Modeling, ...
- Scales up to 100s GB/s, millions of IOPS, sub-ms latencies.

### 5.13. EC2 Instance Storage Summary

- EBS volumes:
  - Network drives attached to one EC2 instance at a time
  - Mapped to an Availability Zones
  - Can use EBS Snapshots for backups / transferring EBS volumes across AZ
- AMI: create ready-to-use EC2 instances with our customizations
- EC2 Image Builder: automatically build, test and distribute AMIs
- EC2 Instance Store:
  - High performance hardware disk attached to our EC2 instance
  - Lost if our instance is stopped / terminated
- EFS: network file system, can be attached to 100s of instances in a region
- EFS-IA: cost-optimized storage class for infrequent accessed files
- FSx for Windows: Network File System for Windows servers
- FSx for Lustre: High Performance Computing Linux file system

## 6. Elastic Load Balancing & Auto Scaling Groups

### 6.1. Scalability & High Availability

- Scalability means that an application / system can handle greater loads by adapting.
- There are two kinds of scalability:
  - Vertical Scalability
  - Horizontal Scalability (= elasticity)
- **Scalability is linked but different to High Availability**

#### 6.1.1. Vertical Scalability

- Let's deep dive into the distinction, using a call center as an example.
- Vertical Scalability means increasing the size of the instance.
- For example, your application runs on a t2.micro.
- Scaling that application vertically means running it on a t2.large.
- Vertical scalability is very common for non distributed systems, such as a database.
- There's usually a limit to how much you can vertically scale (hardware limit).

#### 6.1.2. Horizontal Scalability

- Horizontal Scalability means increasing the number of instances / systems for your application.
- Horizontal scaling implies distributed systems. - This is very common for web applications / modern applications.
- It's easy to horizontally scale thanks the cloud offerings such as Amazon EC2.

### 6.2. High Availability

- High Availability usually goes hand in hand with horizontal scaling.
- High availability means running your application / system in at least 2 Availability Zones.
- The goal of high availability is to survive a data center loss (disaster).

### 6.3. High Availability & Scalability For EC2

- Vertical Scaling: Increase instance size (= scale up / down).
  - From: t2.nano - 0.5G of RAM, 1 vCPU
  - To: u-12tb1.metal - 12.3 TB of RAM, 448 vCPUs
- Horizontal Scaling: Increase number of instances (= scale out / in).
  - Auto Scaling Group
  - Load Balancer
- High Availability: Run instances for the same application across multi AZ.
  - Auto Scaling Group multi AZ
  - Load Balancer multi AZ

### 6.4. Scalability vs Elasticity (vs Agility)

- **Scalability:** ability to accommodate a larger load by making the hardware stronger (scale up), or by adding nodes (scale out).
- **Elasticity:** once a system is scalable, elasticity means that there will be some "auto-scaling" so that the system can scale based on the load. This is "cloud-friendly": pay-per-use, match demand, optimize costs.
- **Agility:** (not related to scalability - distractor) new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes.

### 6.5. What is load balancing?

- Load balancers are servers that forward internet traffic to multiple servers (EC2 Instances) downstream.

### 6.6. Why use a load balancer?

- Spread load across multiple downstream instances
- Expose a single point of access (DNS) to your application
- Seamlessly handle failures of downstream instances
- Do regular health checks to your instances
- Provide SSL termination (HTTPS) for your websites
- High availability across zones

### 6.7. Why use an Elastic Load Balancer (ELB)?

- An ELB (Elastic Load Balancer) is a managed load balancer
  - AWS guarantees that it will be working
  - AWS takes care of upgrades, maintenance, high availability
  - AWS provides only a few configuration knobs
- It costs less to setup your own load balancer but it will be a lot more
  effort on your end (maintenance, integrations)
- 3 kinds of load balancers offered by AWS:
  - Application Load Balancer (HTTP / HTTPS only) - Layer 7
  - Network Load Balancer (ultra-high performance, allows for TCP) - Layer 4
  - Classic Load Balancer (slowly retiring) - Layer 4 & 7

### 6.8. What's an Auto Scaling Group?

- In real-life, the load on your websites and application can change
- In the cloud, you can create and get rid of servers very quickly
- The goal of an Auto Scaling Group (ASG) is to:
  - Scale out (add EC2 instances) to match an increased load
  - Scale in (remove EC2 instances) to match a decreased load
  - Ensure we have a minimum and a maximum number of machines running
  - Automatically register new instances to a load balancer
  - Replace unhealthy instances
- Cost Savings: only run at an optimal capacity (principle of the cloud)

### 6.9. Auto Scaling Groups - Scaling Strategies

- Manual Scaling: Update the size of an ASG manually
- Dynamic Scaling: Respond to changing demand
  - Simple / Step Scaling
    - When a CloudWatch alarm is triggered (example CPU > 70%), then add 2 units
    - When a CloudWatch alarm is triggered (example CPU < 30%), then remove 1
- Target Tracking Scaling
  - Example: I want the average ASG CPU to stay at around 40%
- Scheduled Scaling
  - Anticipate a scaling based on known usage patterns
  - Example: increase the min. capacity to 10 at 5 pm on Fridays
- Predictive Scaling
  - Uses Machine Learning to predict future traffic ahead of time.
  - Automatically provisions the right number of EC2 instances in advance.
  - Useful when your load has predictable time-based patterns.

### 6.10. ELB & ASG - Summary

- High Availability vs Scalability (vertical and horizontal) vs Elasticity vs Agility in the Cloud.
- Elastic Load Balancers (ELB):
  - Distribute traffic across backend EC2 instances, can be Multi-AZ
  - Supports health checks
  - 3 types: Application LB (HTTP - L7), Network LB (TCP - L4), Classic LB (old)
- Auto Scaling Groups (ASG):
  - Implement Elasticity for your application, across multiple AZ
  - Scale EC2 instances based on the demand on your system, replace unhealthy
  - Integrated with the ELB

## 7. Amazon S3

### 7.1. Introduction

- Amazon S3 is one of the main building blocks of AWS
- It's advertised as "infinitely scaling" storage
- Many websites use Amazon S3 as a backbone
- Many AWS services use Amazon S3 as an integration as well
- We'll have a step-by-step approach to S3

### 7.2. S3 Use cases

- Backup and storage
- Disaster Recovery
- Archive
- Hybrid Cloud storage
- Application hosting
- Media hosting
- Data lakes & big data analytics
- Software delivery
- Static website

### 7.3. Amazon S3 Overview

#### 7.3.1. Buckets

- Amazon S3 allows people to store objects (files) in "buckets" (directories)
- Buckets must have a globally unique name (across all regions all accounts)
- Buckets are defined at the region level
- S3 looks like a global service but buckets are created in a region
- Naming convention
  - No uppercase
  - No underscore
  - 3-63 characters long
  - Not an IP
  - Must start with lowercase letter or number

#### 7.3.2. Objects

- Objects (files) have a Key
- The **key** is the **FULL** path:
  - s3://my-bucket/my_file.txt
  - s3://my-bucket/my_folder1/another_folder/my_file.txt
- The key is composed of prefix + object name
  - s3://my-bucket/my_folder1/another_folder/my_file.txt
- There's no concept of "directories" within buckets (although the UI will trick you to think otherwise)
- Just keys with very long names that contain slashes ("/")
- Object values are the content of the body:
  - Max Object Size is 5TB (5000GB)
  - If uploading more than 5GB, must use "multi-part upload"
- **Metadata** (list of text key / value pairs - system or user metadata)
- **Tags** (Unicode key / value pair - up to 10) - useful for security / lifecycle
- Version ID (if versioning is enabled)

### 7.4. S3 Security

- User based
  - IAM policies - which API calls should be allowed for a specific user from IAM console
- Resource Based
  - Bucket Policies - bucket wide rules from the S3 console - allows cross account
  - Object Access Control List (ACL) - finer grain
  - Bucket Access Control List (ACL) - less common
- Note: an IAM principal can access an S3 object if
  - The user IAM permissions allow it OR the resource policy ALLOWS it
  - AND there's no explicit DENY
- Encryption: encrypt objects in Amazon S3 using encryption keys

#### 7.4.1. S3 Bucket Policies

- JSON based policies
  - Resources: buckets and objects
  - Actions: Set of API to Allow or Deny
  - Effect: Allow / Deny
  - Principal: The account or user to apply the policy to
- Use S3 bucket for policy to:
  - Grant public access to the bucket
  - Force objects to be encrypted at upload
  - Grant access to another account (Cross Account)

```
{
    "Version": "2012-10-17",
    "Id": "Policy1648843736704",
    "Statement": [
        {
            "Sid": "Stmt1648843733338",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::test-bucket-jefte-goes/*"
        }
    ]
}
```

#### 7.4.2. Bucket settings for Block Public Access

![Settings for Block Public Access](/Images/EditBlockPublicAccess.PNG)

- These settings were created to prevent company data leaks
- If you know your bucket should never be public, leave these on
- Can be set at the account level

### 7.5. S3 Websites

- S3 can host static websites and have them accessible on the www
- The website URL will be:
  - <bucket-name>.s3-website-<AWS-region>.amazonaws.com
    - OR
  - <bucket-name>.s3-website.<AWS-region>.amazonaws.com
- If you get a 403 (Forbidden) error, make sure the bucket policy allows public reads!

### 7.6. Amazon S3 - Versioning

- You can version your files in Amazon S3
- It is enabled at the **bucket level**
- Same key overwrite will increment the "version": 1, 2, 3...
- It is best practice to version your buckets
  - Protect against unintended deletes (ability to restore a version)
  - Easy roll back to previous version
- Notes:
  - Any file that is not versioned prior to enabling versioning will have version "null"
  - Suspending versioning does not delete the previous versions

### 7.7. S3 Access Logs

- For audit purpose, you may want to log all access to S3 buckets
- Any request made to S3, from any account, authorized or denied, will be logged into another S3 bucket
- That data can be analyzed using data analysis tools...
- Very helpful to come down to the root cause of an issue, or audit usage, view suspicious patterns, etc...

### 7.8. S3 Replication (CRR & SRR)

- Must enable versioning in source and destination
- Cross Region Replication (CRR)
- Same Region Replication (SRR)
- Buckets can be in different accounts
- Copying is asynchronous
- Must give proper IAM permissions to S3
- CRR - Use cases: compliance, lower latency access, replication across accounts
- SRR - Use cases: log aggregation, live replication between production and test accounts

### 7.9. S3 Storage Classes

- Amazon S3 Standard - General Purpose
- Amazon S3 Standard-Infrequent Access (IA)
- Amazon S3 One Zone-Infrequent Access
- Amazon S3 Intelligent Tiering
- Amazon Glacier
- Amazon Glacier Deep Archive
- Amazon S3 Reduced Redundancy Storage (deprecated - omitted)

### 7.10. S3 Durability and Availability

- Durability:
  - High durability (99.999999999%, 11 9's) of objects across multiple AZ
  - If you store 10,000,000 objects with Amazon S3, you can on average expect to incur a loss of a single object once every 10,000 years
  - Same for all storage classes
- Availability:
  - Measures how readily available a service is
  - S3 standard has 99.99% availability, which means it will not be available 53 minutes a year
  - Varies depending on storage class

### 7.11. S3 Standard - General Purposes

- 99.99% Availability
- Used for frequently accessed data
- Low latency and high throughput
- Sustain 2 concurrent facility failures
- Use Cases: Big Data analytics, mobile & gaming applications, content distribution...

### 7.12. S3 Standard - Infrequent Access (IA)

- Suitable for data that is less frequently accessed, but requires rapid access when needed
- 99.9% Availability
- Lower cost compared to Amazon S3 Standard, but retrieval fee
- Sustain 2 concurrent facility failures
- Use Cases: As a data store for disaster recovery, backups...
- **Amazon S3 Standard-Infrequent Access allow you to store infrequently accessed data, with rapid access when needed, has a high durability, and is stored in several Availability Zones to avoid data loss in case of a disaster. It can be used to store data for disaster recovery, backups, etc.**

### 7.13. S3 Intelligent-Tiering

- 99.9% Availability
- Same low latency and high throughput performance of S3 Standard
- Cost-optimized by automatically moving objects between two access
  tiers based on changing access patterns:
  - Frequent access
  - Infrequent access
- Resilient against events that impact an entire Availability Zone

### 7.14. S3 One Zone - Infrequent Access (IA)

- Same as IA but data is stored in a single AZ
- 99.5% Availability
- Low latency and high throughput performance
- Lower cost compared to S3-IA (by 20%)
- Use Cases: Storing secondary backup copies of on-premise data, or storing data you can recreate

### 7.15. Amazon Glacier & Glacier Deep Archive

- Low cost object storage (in GB/month) meant for archiving / backup
- Data is retained for the longer term (years)
- Various retrieval options of time + fees for retrieval:
- Amazon Glacier - cheap:
  - Expedited (1 to 5 minutes)
  - Standard (3 to 5 hours)
  - Bulk (5 to 12 hours)
- Amazon Glacier Deep Archive - cheapest:
  - Standard (12 hours)
  - Bulk (48 hours)

### 7.16. S3 Storage Classes Comparison

|                                    |      S3 Standard       | S3 Intelligent-Tiering |     S3 Standard-IA     |    S3 One Zone-IA†     | S3 Glacier Instant Retrieval | S3 Glacier Flexible Retrieval | S3 Glacier Deep Archive |
| :--------------------------------: | :--------------------: | :--------------------: | :--------------------: | :--------------------: | :--------------------------: | :---------------------------: | :---------------------: |
|      Designed for durability       | 99.999999999% (11 9's) | 99.999999999% (11 9's) | 99.999999999% (11 9's) | 99.999999999% (11 9's) |    99.999999999% (11 9's)    |    99.999999999% (11 9's)     | 99.999999999% (11 9's)  |
|     Designed for availability      |         99.99%         |         99.9%          |         99.9%          |         99.5%          |            99.9%             |            99.99%             |         99.99%          |
|          Availability SLA          |         99.9%          |          99%           |          99%           |          99%           |             99%              |             99.%              |          99.9%          |
|         Availability Zones         |           ≥3           |           ≥3           |           ≥3           |           1            |              ≥3              |              ≥3               |           ≥3            |
| Minimum capacity charge per object |          N/A           |          N/A           |         128 KB         |         128 KB         |            128 KB            |             40 KB             |          40 KB          |
|  Minimum storage duration charge   |          N/A           |          N/A           |        30 days         |        30 days         |           90 days            |            90 days            |        180 days         |
|          Retrieval charge          |          N/A           |          N/A           |    per GB retrieved    |    per GB retrieved    |       per GB retrieved       |       per GB retrieved        |    per GB retrieved     |
|         First byte latency         |      milliseconds      |      milliseconds      |      milliseconds      |      milliseconds      |         milliseconds         |       minutes or hours        |          hours          |
|            Storage type            |         Object         |         Object         |         Object         |         Object         |            Object            |            Object             |         Object          |
|       Lifecycle transitions        |          Yes           |          Yes           |          Yes           |          Yes           |             Yes              |              Yes              |           Yes           |

### 7.17. Moving between storage classes

- You can transition objects between storage classes
- For infrequently accessed object, move them to STANDARD_IA
- For archive objects you don't need in real-time, GLACIER or DEEP_ARCHIVE
- Moving objects can be automated using a **lifecycle configuration**

### 7.18. S3 Object Lock & Glacier Vault Lock

- S3 Object Lock
  - Adopt a WORM (Write Once Read Many) model
  - Block an object version deletion for a specified amount of time
- Glacier Vault Lock
  - Adopt a WORM (Write Once Read Many) model
  - Lock the policy for future edits (can no longer be changed)
  - Helpful for compliance and data retention

### 7.19. S3 Encryption

- Types:
  - No Encryption
  - Server-Side Encryption
  - Client-Side Encryption

### 7.20. Shared Responsibility Model for S3

- Aws:
  - Infrastructure (global security, durability, availability, sustain concurrent loss of data in two facilities)
  - Configuration and vulnerability analysis
  - Compliance validation
- You:
  - S3 Versioning
  - S3 Bucket Policies
  - S3 Replication Setup
  - Logging and Monitoring
  - S3 Storage Classes
  - Data encryption at rest and in transit

### 7.21. AWS Snow Family

- Highly-secure, portable devices to collect and process data at the edge, and migrate data into and out of AWS
  - Data migration:
    - Snowcon
    - Snowball Edge
    - Snowmobile
  - Edge computing:
    - Snowcone
    - Snowball Edge

### 7.22. Data Migrations with AWS Snow Family

- Challenges:

  - Limited connectivity
  - Limited bandwidth
  - High network cost
  - Shared bandwidth (can't maximize the line)
  - Connection stability

- Time to Transfer:

|        | 100 Mbps | 1Gbps    | 10Gbps   |
| ------ | -------- | -------- | -------- |
| 10 TB  | 12 days  | 30 hours | 3 hours  |
| 100 TB | 124 days | 12 days  | 30 hours |
| 1 PB   | 3 years  | 124 days | 12 days  |

- AWS Snow Family: offline devices to perform data migrations

  - If it takes more than a week to transfer over the network, use Snowball devices!

#### 7.22.1. AWS Snowcone

- Small, portable computing, anywhere, rugged & secure, withstands harsh environments
- Light (4.5 pounds, 2.1 kg)
- Device used for edge computing, storage, and data transfer
- 8 TBs of usable storage
- Use Snowcone where Snowball does not fit (space-constrained environment)
- Must provide your own battery / cables
- Can be sent back to AWS offline, or connect it to internet and use AWS DataSync to send data

#### 7.22.2. Snowball Edge (for data transfers)

- Physical data transport solution: move TBs or PBs of data in or out of AWS
- Alternative to moving data over the network (and paying network fees)
- Pay per data transfer job
- Provide block storage and Amazon S3-compatible object storage
- Snowball Edge Storage Optimized
  - 80 TB of HDD capacity for block volume and S3 compatible object storage
- Snowball Edge Compute Optimized
  - 42 TB of HDD capacity for block volume and S3 compatible object storage
- Use cases: large data cloud migrations, DC decommission, disaster recovery
- **Snowball Edge is best-suited to move petabytes of data and offers computing capabilities. Be careful, it's recommended to use a fleet of Snowballs to move less than 10PBs of data. Over this quantity, it's better-suited to use Snowmobile.**

#### 7.22.3. AWS Snowmobile

- Transfer exabytes of data (1 EB = 1,000 PB = 1,000,000 TBs)
- Each Snowmobile has 100 PB of capacity (use multiple in parallel)
- High security: temperature controlled, GPS, 24/7 video surveillance
- Better than Snowball if you transfer more than 10 PB

### 7.23. Snow Family - Usage Process

1. Request Snowball devices from the AWS console for delivery
2. Install the snowball client / AWS OpsHub on your servers
3. Connect the snowball to your servers and copy files using the client
4. Ship back the device when you're done (goes to the right AWS facility)
5. Data will be loaded into an S3 bucket
6. Snowball is completely wiped

### 7.24. What is Edge Computing?

- Process data while it's being created on an edge location
  - A truck on the road, a ship on the sea, a mining station underground...
- These locations may have
  - Limited / no internet access
  - Limited / no easy access to computing power
- We setup a Snowball Edge / Snowcone device to do edge computing
- Use cases of Edge Computing:
  - Preprocess data
  - Machine learning at the edge
  - Transcoding media streams
- Eventually (if need be) we can ship back the device to AWS (for transferring data for example)

### 7.25. Snow Family - Edge Computing

- Snowcone (smaller)
  - 2 CPUs, 4 GB of memory, wired or wireless access
  - USB-C power using a cord or the optional battery
- Snowball Edge - Compute Optimized
  - 52 vCPUs, 208 GiB of RAM
  - Optional GPU (useful for video processing or machine learning)
  - 42 TB usable storage
- Snowball Edge - Storage Optimized
  - Up to 40 vCPUs, 80 GiB of RAM
  - Object storage clustering available
- All: Can run EC2 Instances & AWS Lambda functions (using AWS IoT Greengrass)
- Long-term deployment options: 1 and 3 years discounted pricing

### 7.26. AWS OpsHub

- Historically, to use Snow Family devices, you needed a CLI (Command Line Interface tool)
- Today, you can use AWS OpsHub (a software you install on your computer / laptop) to manage your Snow Family Device
  - Unlocking and configuring single or clustered devices
  - Transferring files
  - Launching and managing instances running on Snow Family Devices
- Monitor device metrics (storage capacity, active instances on your device)
- Launch compatible AWS services on your devices (ex: Amazon EC2 instances, AWS DataSync, Network File System (NFS))

### 7.27. Hybrid Cloud for Storage

- AWS is pushing for "hybrid cloud"
  - Part of your infrastructure is on-premises
  - Part of your infrastructure is on the cloud
- This can be due to
  - Long cloud migrations
  - Security requirements
  - Compliance requirements
  - IT strategy
- S3 is a proprietary storage technology (unlike EFS / NFS), so how do you expose the S3 data on-premise?
- AWS Storage Gateway!

### 7.28. AWS Storage Gateway

- Bridge between on-premise data and cloud data in S3
- Hybrid storage service to allow on- premises to seamlessly use the AWS Cloud
- Use cases: disaster recovery, backup & restore, tiered storage
- Types of Storage Gateway:
  - File Gateway
  - Volume Gateway
  - Tape Gateway

### 7.29. Amazon S3 - Summary

- Buckets vs Objects: global unique name, tied to a region.
- S3 security: IAM policy, S3 Bucket Policy (public access), S3 Encryption.
- S3 Websites: host a static website on Amazon S3.
- S3 Versioning: multiple versions for files, prevent accidental deletes.
- S3 Access Logs: log requests made within your S3 bucket.
- S3 Replication: same-region or cross-region, must enable versioning.
- S3 Storage Classes: Standard, IA, 1Z-IA, Intelligent, Glacier, Glacier Deep Archive.
- S3 Lifecycle Rules: transition objects between classes.
- S3 Glacier Vault Lock / S3 Object Lock: WORM (Write Once Read Many).
- Snow Family: import data onto S3 through a physical device, edge computing.
- OpsHub: desktop application to manage Snow Family devices.
- Storage Gateway: hybrid solution to extend on-premises storage to S3.

## 8. Databases

### 8.1. Introduction

- Storing data on disk (EFS, EBS, EC2 Instance Store, S3) can have its limits.
- Sometimes, you want to store data in a database...
- You can **structure** the data.
- You build **indexes** to efficiently **query / search** through the data.
- You define **relationships** between your **datasets**.
- Databases are **optimized for a purpose** and come with different features, shapes and constraints.

### 8.2. Relational Databases

- Looks just like Excel spreadsheets, with links between them!
- Can use the SQL language to perform queries / lookups.

### 8.3. NoSQL Databases

- NoSQL = non-SQL = non relational databases
- NoSQL databases are purpose built for specific data models and have flexible schemas for building modern applications.
- Benefits:
  - Flexibility: easy to evolve data model.
  - Scalability: designed to scale-out by using distributed clusters.
  - High-performance: optimized for a specific data model.
  - Highly functional: types optimized for the data model.
- Examples: Key-value, document, graph, in-memory, search databases.

### 8.4. NoSQL data example: JSON

- JSON = JavaScript Object Notation.
- JSON is a common form of data that fits into a NoSQL model.
- Data can be nested.
- Fields can change over time.
- Support for new types: arrays, etc...

```
{
   "name":"John",
   "age":30,
   "cars":[
      "Ford",
      "BMW",
      "Fiat"
   ],
   "address":{
      "type":"house",
      "number":23,
      "street":"Dream Road"
   }
}
```

### 8.5. Databases & Shared Responsibility on AWS

- AWS offers use to **manage** different databases.
- **Databases** & Shared Responsibility on AWS include:
  - Quick Provisioning, High Availability, Vertical and Horizontal Scaling.
  - Automated Backup & Restore, Operations, Upgrades.
  - Operating System Patching is handled by AWS.
  - Monitoring, alerting.
- Note: many databases technologies could be run on EC2, but you must handle yourself the resiliency, backup, patching, high availability, fault tolerance, scaling...

### 8.6. AWS RDS Overview

- **Amazon Relational Database Service (Amazon RDS) is a SQL managed service that makes it easy to set up, operate, and scale a relational database in the cloud. It is suited for OLTP workloads.**
- RDS stands for Relational Database Service.
- It's a managed DB service for DB use SQL as a query language.
- It allows you to create databases in the cloud that are managed by AWS:
  - Postgres
  - MySQL
  - MariaDB
  - Oracle
  - Microsoft SQL Server
  - Aurora (AWS Proprietary database)

### 8.7. Advantage over using RDS versus deploying DB on EC2

- RDS is a managed service:
  - Automated provisioning, OS patching.
  - Continuous backups and restore to specific timestamp (Point in Time Restore)!
  - Monitoring dashboards.
  - Read replicas for improved read performance.
  - Multi AZ setup for DR (Disaster Recovery).
  - Maintenance windows for upgrades.
  - Scaling capability (vertical and horizontal).
  - Storage backed by EBS (gp2 or io1).
- BUT you can't SSH into your instances.

### 8.8. Amazon Aurora

- **Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. It is a proprietary technology from AWS.**
- Aurora is a proprietary technology from AWS (not open sourced).
- **PostgreSQL and MySQL** are both supported as Aurora DB.
- Aurora is "AWS cloud optimized" and claims 5x performance improvement over MySQL on RDS, over 3x the performance of Postgres on RDS.
- Aurora storage automatically grows in increments of 10GB, up to 64 TB.
- Aurora costs more than RDS (20% more) - but is more efficient.
- Not in the free tier.

### 8.9. RDS Deployments: Read Replicas, Multi-AZ, Multi-Region

#### 8.9.1. Read Replicas

- Scale the read workload of your DB
- Can create up to 5 Read Replicas
- Data is only written to the main DB

#### 8.9.2. Multi-AZ

- Failover in case of AZ outage (high availability)
- Data is only read/written to the main database
- Can only have 1 other AZ as failover

#### 8.9.3. Multi-Region

- Multi-Region (Read Replicas)
- Disaster recovery in case of region issue
- Local performance for global reads
- Replication cost

#### 8.9.4. Resume

- **RDS Multi-AZ deployments main purpose is high availability, and RDS Read replicas main purpose is scalability. Moreover, Multi-Region deployments' main purpose is disaster recovery and local performance.**

### 8.10. Amazon ElastiCache Overview

- **Amazon ElastiCache is a web service that makes it easy to deploy and run Memcached or Redis protocol-compliant server nodes in the cloud. ElastiCache caches are in-memory databases with high performance, low latency. They help reduce load off databases for read intensive workloads.**
- The same way RDS is to get managed Relational Databases...
- ElastiCache is to get managed Redis or Memcached.
- Helps **reduce load off databases for read intensive workloads**.
- AWS takes care of OS maintenance / patching, optimizations, setup, configuration, monitoring, failure recovery and backups.

### 8.11. DynamoDB

- **DynamoDB is a fast and flexible non-relational database service for any scale. It can scale with no downtime, it can process millions of requests per second, and is fast and consistent in performance.**
- Fully Managed Highly available with replication across 3 AZ.
- **NoSQL database - not a relational database.**
- Scales to massive workloads, distributed **"serverless**" database.
- Millions of requests per seconds, trillions of row, 100s of TB of storage.
- Fast and consistent in performance.
- **Single-digit millisecond latency - low latency retrieval.**
- Integrated with IAM for security, authorization and administration.
- Low cost and auto scaling capabilities.

#### 8.11.1. DynamoDB Accelerator - DAX

- **Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB that delivers up to a 10 times performance improvement—from milliseconds to microseconds—even at millions of requests per second.**
- Fully Managed **in-memory** cache for DynamoDB.
- **10x performance improvement** - single- digit millisecond latency to microseconds latency - when accessing your DynamoDB tables.
- Secure, highly scalable & highly available.
- Difference with ElastiCache at the CCP level: DAX is only used for and is integrated with DynamoDB, while ElastiCache can be used for other databases.

#### 8.11.2. DynamoDB - Global Tables

- Make a DynamoDB table accessible with low latency in multiple-regions.
- Active-Active replication (read/write to any AWS Region).

### 8.12. Redshift Overview

- **Amazon Redshift is a fully managed, petabyte-scale data warehouse service in the cloud.**
- Redshift is based on PostgreSQL, but it's not used for OLTP.
- **It's OLAP - online analytical processing (analytics and data warehousing).**
- Load data once every hour, not every second.
- 10x better performance than other data warehouses, scale to PBs of data.
- **Columnar** storage of data (instead of row based).
- Massively Parallel Query Execution (MPP), highly available.
- Pay as you go based on the instances provisioned.
- Has a SQL interface for performing the queries.
- BI tools such as AWS Quicksight or Tableau integrate with it.
- **Manage their data warehouse.**

### 8.13. Amazon EMR

- EMR stands for "Elastic MapReduce"
- **Amazon EMR is a web service that enables businesses, researchers, data analysts, and developers to easily and cost-effectively process vast amounts of data. EMR helps creating Hadoop clusters (Big Data) to analyze and process vast amount of data.**
- The clusters can be made of hundreds of EC2 instances
- Also supports Apache Spark, HBase, Presto, Flink...
- EMR takes care of all the provisioning and configuration
- Auto-scaling and integrated with Spot instances
- Use cases: data processing, machine learning, web indexing, big data...

### 8.14. Amazon Athena

- **Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run.**
- Serverless query service to analyze data stored in Amazon S3.
- Uses standard SQL language to query the files.
- Supports CSV, JSON, ORC, Avro, and Parquet (built on Presto).
- Pricing: $9.00 per TB of data scanned (2022).
- Use compressed or columnar data for cost-savings (less scan).
- Use cases: Business intelligence / analytics / reporting, analyze & query VPC Flow Logs, ELB Logs, CloudTrail trails, etc...
- Tip: analyze data in S3 using serverless SQL, use Athena.

### 8.15. Amazon QuickSight

- **Amazon QuickSight is a fast, cloud-powered business intelligence (BI) service that makes it easy for you to deliver insights to everyone in your organization. You can create and publish interactive dashboards.**
- Serverless machine learning-powered business intelligence service to create interactive dashboards.
- Fast, automatically scalable, embeddable, with per-session pricing.
- Use cases:
  - Business analytics
  - Building visualizations
  - Perform ad-hoc analysis
  - Get business insights using data
- Integrated with RDS, Aurora, Athena, Redshift, S3...

### 8.16. DocumentDB

- **Amazon DocumentDB (with MongoDB compatibility) is a fast, calable, highly available, and fully managed document database service that supports MongoDB workloads.**
- Aurora is an "AWS-implementation" of PostgreSQL / MySQL...
- **DocumentDB is the same for MongoDB (which is a NoSQL database).**
- MongoDB is used to store, query, and index JSON data.
- Similar "deployment concepts" as Aurora.
- Fully Managed, highly available with replication across 3 AZ.
- Aurora storage automatically grows in increments of 10GB, up to 64 TB.
- Automatically scales to workloads with millions of requests per seconds.

### 8.17. Amazon Neptune

- **Amazon Neptune is a fast, reliable, fully-managed graph database service that makes it easy to build and run applications that work with highly connected datasets. It can be used for knowledge graphs, fraud detection, recommendations engines, social networking, etc.**
- Fully managed graph database.
- A popular graph dataset would be a social network.
  - Users have friends
  - Posts have comments
  - Comments have likes from users
  - Users share and like posts...
- Highly available across 3 AZ, with up to 15 read replicas.
- Build and run applications working with highly connected datasets - optimized for these complex and hard queries.
- Can store up to billions of relations and query the graph with milliseconds latency.
- Highly available with replications across multiple AZs.

### 8.18. Amazon QLDB

- QLDB stands for "Quantum Ledger Database".
- **Amazon QLDB is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log owned by a central trusted authority. Amazon QLDB tracks each and every application data change and maintains a complete and verifiable history of changes over time.**
- A ledger is a book recording financial transactions.
- Fully Managed, Serverless, High available, Replication across 3 AZ.
- Used to review history of all the changes made to your application data over time.
- Immutable system: no entry can be removed or modified, cryptographically verifiable.
- 2-3x better performance than common ledger blockchain frameworks, manipulate data using SQL.
- Difference with Amazon Managed Blockchain: no decentralization component, in accordance with financial regulation rules.

### 8.19. Amazon Managed Blockchain

- Amazon Managed Blockchain is a fully managed service that makes it easy to create and manage scalable blockchain networks using the popular open source frameworks Hyperledger Fabric and Ethereum. It allows multiple parties to execute transactions without the need of a trusted, central authority.
- Blockchain makes it possible to build applications where multiple parties can execute transactions without the need for a trusted, central authority.
- Amazon Managed Blockchain is a managed service to:
  - Join public blockchain networks
  - Or create your own scalable private network
- Compatible with the frameworks Hyperledger Fabric & Ethereum

### 8.20. AWS Glue

- **AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics.**
- Managed extract, transform, and load (ETL) service.
- Useful to prepare and transform data for analytics.
- Fully serverless service.
- Glue Data Catalog: catalog of datasets.
  - **The AWS Glue Data Catalog is a central repository to store structural and operational metadata for all your data assets. For a given data set, you can store its table definition, physical location, add business relevant attributes, as well as track how this data has changed over time.**
  - Can be used by Athena, Redshift, EMR.

### 8.21. DMS - Database Migration Service

- **AWS Database Migration Service helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database.**
- Quickly and securely migrate databases to AWS, resilient, self healing
- The source database remains available during the migration
- Supports:
  - Homogeneous migrations: ex Oracle to Oracle
  - Heterogeneous migrations: ex Microsoft SQL Server to Aurora

### 8.22. Databases & Analytics Summary in AWS

- Relational Databases - OLTP: RDS & Aurora (SQL).
- Differences between Multi-AZ, Read Replicas, Multi-Region.
- In-memory Database: ElastiCache.
- Key/Value Database: DynamoDB (serverless) & DAX (cache for DynamoDB).
- Warehouse - OLAP: Redshift (SQL).
- Hadoop Cluster: EMR.
- Athena: query data on Amazon S3 (serverless & SQL).
- QuickSight: dashboards on your data (serverless).
- DocumentDB: "Aurora for MongoDB" (JSON - NoSQL database).
- Amazon QLDB: Financial Transactions Ledger (immutable journal, cryptographically verifiable).
- Amazon Managed Blockchain: managed Hyperledger Fabric & Ethereum blockchains.
- Glue: Managed ETL (Extract Transform Load) and Data Catalog service.
- Database Migration: DMS.
- Neptune: Graph database.

## 9. Other Compute Services: ECS, Lambda, Batch, Lightsail

### 9.1. ECS

- ECS = Elastic Container Service.
- Launch Docker containers on AWS.
- **You must provision & maintain the infrastructure (the EC2 instances)**.
- AWS takes care of starting / stopping containers.
- Has integrations with the Application Load Balancer.

### 9.2. Fargate

- Launch Docker containers on AWS.
- **You do not provision the infrastructure (no EC2 instances to manage)**.
- Serverless offering.
- AWS just runs containers for you based on the CPU / RAM you need.

### 9.3. ECR

- Elastic Container Registry.
- Private Docker Registry on AWS.
- This is where you store your Docker images so they can be run by ECS or Fargate.

### 9.4. What's serverless?

- Serverless is a new paradigm in which the developers don't have to manage servers anymore.
- They just deploy code / functions.
- Initially... Serverless == FaaS (Function as a Service)
- Serverless was pioneered by AWS Lambda but now also includes anything that's managed: "databases, messaging, storage, etc."
- Serverless does not mean there are no servers... it means you just don't manage / provision / see them
- Serverless:
  - Amazon S3
  - DynamoDB
  - Fargate
  - Lambda

### 9.5. Why AWS Lambda?

- Amazon EC2:
  - Virtual Servers in the Cloud.
  - Limited by RAM and CPU.
  - Continuously running.
  - Scaling means intervention to add / remove servers.
- Amazon Lambda:
  - Virtual functions - no servers to manage!
  - Limited by time - short executions.
  - Run on-demand.
  - Scaling is automated!

#### 9.5.1. Benefits of AWS Lambda

- Easy Pricing:
  - Pay per request and compute time.
  - Free tier of 1,000,000 AWS Lambda requests and 400,000 GBs of compute time.
- Integrated with the whole AWS suite of services.
- **Event-Driven**: functions get invoked by AWS when needed.
- Integrated with many programming languages.
- Easy monitoring through AWS CloudWatch.
- Easy to get more resources per functions (up to 10GB of RAM!).
- Increasing RAM will also improve CPU and network!

#### 9.5.2. AWS Lambda language support

- Node.js (JavaScript)
- Python
- Java (Java 8 compatible)
- C# (.NET Core)
- Golang
- C# / Powershell
- Ruby
- Custom Runtime API (community supported, example Rust)
- Lambda Container Image
  - The container image must implement the Lambda Runtime API
  - ECS / Fargate is preferred for running arbitrary Docker images

#### 9.5.3. AWS Lambda Pricing: example

- You can find overall pricing information here: https://aws.amazon.com/lambda/pricing/
- Pay per **calls**:
  - First 1,000,000 requests are free.
  - $0.20 per 1 million requests thereafter ($0.0000002 per request).
- Pay per **duration**: (in increment of 1 ms)
  - 400,000 GB-seconds of compute time per month for FREE.
  - == 400,000 seconds if function is 1GB RAM.
  - == 3,200,000 seconds if function is 128 MB RAM.
  - After that $1.00 for 600,000 GB-seconds.
- It is usually **very cheap** to run AWS Lambda so it's **very popular**.

### 9.6. Amazon API Gateway

- Example: building a serverless API.
- Fully managed service for developers to easily create, publish, maintain, monitor, and secure APIs.
- Serverless and scalable.
- Supports RESTful APIs and WebSocket APIs.
- Support for security, user authentication, API throttling, API keys, monitoring...

### 9.7. AWS Batch

- **Fully managed** batch processing at **any scale**.
- Efficiently run 100,000s of computing batch jobs on AWS.
- A "batch" job is a job with a start and an end (opposed to continuous).
- Batch will dynamically launch **EC2 instances** or **Spot Instances**.
- AWS Batch provisions the right amount of compute / memory.
- You submit or schedule batch jobs and AWS Batch does the rest!
- Batch jobs are defined as **Docker images** and **run on ECS**.
- Helpful for cost optimizations and focusing less on the infrastructure.

### 9.8. Batch vs Lambda

- Lambda:
  - Time limit.
  - Limited runtimes.
  - Limited temporary disk space.
  - Serverless.
- Batch:
  - No time limit.
  - Any runtime as long as it's packaged as a Docker image.
  - Rely on EBS / instance store for disk space.
  - Relies on EC2 (can be managed by AWS).

### 9.9. Amazon Lightsail

- **Amazon Lightsail is designed to be the easiest way to launch and manage a virtual private server with AWS. Lightsail plans include everything you need to jumpstart your project - a virtual machine, SSD- based storage, data transfer, DNS management, and a static IP address - for a low, predictable price. It can be used to create a simple web application, a website or a dev/test environment.**
- Virtual servers, storage, databases, and networking.
- Low & predictable pricing.
- Simpler alternative to using EC2, RDS, ELB, EBS, Route 53...
- Great for people with little cloud experience!
- Can setup notifications and monitoring of your Lightsail resources.
- Use cases:
  - Simple web applications (has templates for LAMP, Nginx, MEAN, Node.js...).
  - Websites (templates for WordPress, Magento, Plesk, Joomla).
  - Dev / Test environment.
- Has high availability but no auto-scaling, limited AWS integrations.

### 9.10. Other Compute - Summary

- Docker: container technology to run applications.
- ECS: run Docker containers on EC2 instances.
- Fargate:
  - Run Docker containers without provisioning the infrastructure.
  - Serverless offering (no EC2 instances).
- ECR: Private Docker Images Repository.
- Batch: run batch jobs on AWS across managed EC2 instances.
- Lightsail: predictable & low pricing for simple application & DB stacks.

### 9.11. Lambda Summary

- Lambda is Serverless, Function as a Service, seamless scaling, reactive.
- Lambda Billing:
  - By the time run x by the RAM provisioned.
  - By the number of invocations.
- Language Support: many programming languages except (arbitrary) Docker.
- Invocation time: up to 15 minutes.
- Use cases:
  - Create Thumbnails for images uploaded onto S3.
  - Run a Serverless cron job.
- API Gateway: expose Lambda functions as HTTP API.

## 10. Deploying and Managing Infrastructure at Scale

### 10.1. What is CloudFormation?

- CloudFormation is a declarative way of outlining your AWS Infrastructure, for any resources (most of them are supported).
- For example, within a CloudFormation template, you say:
  - I want a security group.
  - I want two EC2 instances using this security group.
  - I want an S3 bucket.
  - I want a load balancer (ELB) in front of these machines.
- Then CloudFormation creates those for you, in the right order, with the exact configuration that you specify.

#### 10.1.1. Benefits of AWS CloudFormation

**- CloudFormation are free of use, but you do pay for the resources created.**

- Infrastructure as code
  - No resources are manually created, which is excellent for control.
  - Changes to the infrastructure are reviewed through code.
- Cost
  - Each resources within the stack is tagged with an identifier so you can easily see how much a stack costs you.
  - You can estimate the costs of your resources using the CloudFormation template.
  - Savings strategy: In Dev, you could automation deletion of templates at 5 PM and recreated at 8 AM, safely.
- Productivity
  - Ability to destroy and re-create an infrastructure on the cloud on the fly.
  - Automated generation of Diagram for your templates!
  - Declarative programming (no need to figure out ordering and orchestration).
- Don't re-invent the wheel
  - Leverage existing templates on the web!
  - Leverage the documentation.
- Supports (almost) all AWS resources:
  - Everything we'll see in this course is supported.
  - You can use "custom resources" for resources that are not supported.

#### 10.1.2. CloudFormation Stack Designer

- **AWS CloudFormation templates are JSON or YAML-formatted text files. They are declarations of the AWS resources that make up a stack.**
- Example: WordPress CloudFormation Stack.
- We can see all the resources.
- We can see the relations between the components.

### 10.2. AWS Cloud Development Kit (CDK)

- **The AWS Cloud Development Kit (AWS CDK) is an open source software development framework to define your cloud application resources using familiar programming languages.**
  - JavaScript/TypeScript, Python, Java, and .NET.
- The code is "compiled" into a CloudFormation template (JSON/YAML).
- You can therefore deploy infrastructure and application runtime code together.
  - Great for Lambda functions.
  - Great for Docker containers in ECS / EKS.

### 10.3. Developer problems on AWS

- Managing infrastructure.
- Deploying Code.
- Configuring all the databases, load balancers, etc.
- Scaling concerns.
- Most web apps have the same architecture (ALB + ASG).
- All the developers want is for their code to run!
- Possibly, consistently across different applications and environments.

### 10.4. AWS Elastic Beanstalk Overview

- **Elastic Beanstalk is a Platform as a Service (PaaS). You only manage data and applications. AWS Elastic Beanstalk makes it even easier for developers to quickly deploy and manage applications in the AWS Cloud.**
- Elastic Beanstalk is a developer centric view of deploying an application on AWS.
- It uses all the component's we've seen before: EC2, ASG, ELB, RDS, etc...
- But it's all in one view that's easy to make sense of!
- We still have full control over the configuration.
- Beanstalk = Platform as a Service (PaaS).
- **Elastic Beanstalk are free of use, but you do pay for the resources created..**

### 10.5. Elastic Beanstalk

- Managed service
  - Instance configuration / OS is handled by Beanstalk.
  - Deployment strategy is configurable but performed by Elastic Beanstalk.
  - Capacity provisioning.
  - Load balancing & auto-scaling.
  - Application health-monitoring & responsiveness.
- Just the application code is the responsibility of the developer.
- Three architecture models:
  - Single Instance deployment: good for dev.
  - LB + ASG: great for production or pre-production web applications.
  - ASG only: great for non-web apps in production (workers, etc..).
- Support for many platforms:
  - Go
  - Java SE
  - Java with Tomcat
  - .NET on Windows Server with IIS
  - Node.js
  - PHP
  - Python
  - Ruby
  - Packer Builder
- Single Container Docker.
- Multi-Container Docker.
- Preconfigured Docker.

#### 10.5.1. Health Monitoring

- Health agent pushes metrics to CloudWatch.
- Checks for app health, publishes health events.

### 10.6. AWS CodeDeploy

- **AWS CodeDeploy is a service that automates code deployments to any instance, including Amazon EC2 instances and instances running on-premises.**
- We want to deploy our application automatically.
- Hybrid service.
- Servers / Instances must be provisioned and configured ahead of time with the CodeDeploy Agent.

### 10.7. AWS CodeCommit

- **AWS CodeCommit is a secure, highly scalable, managed source control service that makes it easier for teams to collaborate on code. It also provides software version control.**
- Before pushing the application code to servers, it needs to be stored somewhere.
- Developers usually store code in a repository, using the Git technology.
- A famous public offering is GitHub, AWS competing product is CodeCommit.
- CodeCommit:
  - Source-control service that hosts Git-based repositories.
  - Makes it easy to collaborate with others on code.
  - The code changes are automatically versioned.
- Benefits:
  - Fully managed.
  - Scalable & highly available.
  - Private, Secured, Integrated with AWS.

### 10.8. AWS CodeBuild

- **AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy. With CodeBuild, you don't need to provision, manage, and scale your own build servers, it is serverless.**
- Code building service in the cloud (name is obvious)
- Compiles source code, run tests, and produces packages that are ready to be deployed (by CodeDeploy for example)
- Benefits:
  - Fully managed, serverless.
  - Continuously scalable & highly available.
  - Secure.
  - Pay-as-you-go pricing - only pay for the build time.

### 10.9. AWS CodePipeline

- Orchestrate the different steps to have the code automatically pushed to production.
  - Code => Build => Test => Provision => Deploy.
  - Basis for CI/CD (Continuous Integration & Continuous Delivery).
- Benefits:
  - Fully managed, compatible with CodeCommit, CodeBuild, CodeDeploy, Elastic Beanstalk, CloudFormation, GitHub, 3rd-party services (GitHub...) & custom plugins...
- Fast delivery & rapid updates.

### 10.10. AWS CodeArtifact

- **AWS CodeArtifact is a fully managed artifact repository (also called code dependencies) service that makes it easy for organizations of any size to securely store, publish, and share software packages used in their software development process.**
- Software packages depend on each other to be built (also called code dependencies), and new ones are created.
- Storing and retrieving these dependencies is called artifact management.
- Traditionally you need to setup your own artifact management system.
- CodeArtifact is a secure, scalable, and cost-effective artifact management for software development.
- Works with common dependency management tools such as Maven, Gradle, npm, yarn, twine, pip, and NuGet.
- Developers and CodeBuild can then retrieve dependencies straight from CodeArtifact.

### 10.11. AWS CodeStar

- **CodeStar is used to quickly develop, build, and deploy applications on AWS. Elastic Beanstalk can be used to monitor and to check the health of an environment.**
- Unified UI to easily manage software development activities in one place.
- "Quick way" to get started to correctly set-up CodeCommit, CodePipeline, CodeBuild, CodeDeploy, Elastic Beanstalk, EC2, etc...
- Can edit the code "in-the-cloud" using AWS Cloud9.

### 10.12. AWS Cloud9

- AWS Cloud9 is a cloud IDE (Integrated Development Environment) for writing, running and debugging code.
- "Classic" IDE (like IntelliJ, Visual Studio Code...) are downloaded on a computer before being used.
- A cloud IDE can be used within a web browser, meaning you can work on your projects from your office, home, or anywhere with internet with no setup necessary.
- AWS Cloud9 also allows for code collaboration in real-time (pair programming).

### 10.13. AWS Systems Manager (SSM)

- **AWS Systems Manager gives you visibility and control of your infrastructure on AWS. It is used for patching systems at scale.**
- Helps you manage your EC2 and On-Premises systems at scale.
- Another Hybrid AWS service.
- Get operational insights about the state of your infrastructure.
- Suite of 10+ products.
- Most important features are:
  - Patching automation for enhanced compliance.
  - Run commands across an entire fleet of servers.
  - Store parameter configuration with the SSM Parameter Store.
- Works for both Windows and Linux OS.

#### 10.13.1. How Systems Manager works?

- We need to install the SSM agent onto the systems we control.
- Installed by default on Amazon Linux AMI & some Ubuntu AMI.
- If an instance can't be controlled with SSM, it's probably an issue with the SSM agent!
- Thanks to the SSM agent, we can run commands, patch & configure our servers.

#### 10.13.2. Systems Manager - SSM Session Manager

- Allows you to start a secure shell on your EC2 and on-premises servers.
- No SSH access, bastion hosts, or SSH keys needed.
- No port 22 needed (better security).
- Supports Linux, macOS, and Windows.
- Send session log data to S3 or CloudWatch Logs.

### 10.14. AWS OpsWorks

- Chef & Puppet help you perform server configuration automatically, or repetitive actions.
- They work great with EC2 & On-Premises VM.
- AWS OpsWorks = Managed Chef & Puppet.
- It's an alternative to AWS SSM.
- Only provision standard AWS resources:
  - EC2 Instances, Databases, Load Balancers, EBS volumes...
- Tip: Chef or Puppet needed => AWS OpsWorks.

### 10.15. Deployment - Summary

- CloudFormation: (AWS only):
  - Infrastructure as Code, works with almost all of AWS resources.
  - Repeat across Regions & Accounts.
- Beanstalk: (AWS only):
  - Platform as a Service (PaaS), limited to certain programming languages or Docker.
  - Deploy code consistently with a known architecture: ex, ALB + EC2 + RDS.
- CodeDeploy (hybrid): deploy & upgrade any application onto servers.
- Systems Manager (hybrid): patch, configure and run commands at scale.
- OpsWorks (hybrid): managed Chef and Puppet in AWS.
- CodeCommit: Store code in private git repository (version controlled).
- CodeBuild: Build & test code in AWS.
- CodeDeploy: Deploy code onto servers.
- CodePipeline: Orchestration of pipeline (from code to build to deploy).
- CodeArtifact: Store software packages / dependencies on AWS.
- CodeStar: Unified view for allowing developers to do CICD and code.
- Cloud9: Cloud IDE (Integrated Development Environment) with collab.
- AWS CDK: Define your cloud infrastructure using a programming language.

## 11. Global Infrastructure

### 11.1. Why make a global application?

- A **global application** is an application deployed in **multiple geographies**.
- On AWS: this could be **Regions** and / or **Edge Locations**.
- Decreased Latency:
  - Latency is the time it takes for a network packet to reach a server.
  - It takes time for a packet from Asia to reach the US.
  - Deploy your applications closer to your users to decrease latency, better experience.
- Disaster Recovery (DR):
  - If an AWS region goes down (earthquake, storms, power shutdown, politics)...
  - You can fail-over to another region and have your application still working.
  - A DR plan is important to increase the availability of your application.
- Attack protection: distributed global infrastructure is harder to attack

### 11.2. Global AWS Infrastructure

- **Regions:** For deploying applications and infrastructure
- **Availability Zones:** Made of multiple data centers
- **Edge Locations (Points of Presence):** for content delivery as close as possible to users

### 11.3. Global Applications in AWS

- **Global DNS: Route 53**
  - Great to route users to the closest deployment with least latency
  - Great for disaster recovery strategies
- **Global Content Delivery Network (CDN): CloudFront**
  - Replicate part of your application to AWS Edge Locations - decrease latency
  - Cache common requests - improved user experience and decreased latency
- **S3 Transfer Acceleration**
  - Accelerate global uploads & downloads into Amazon S3
- **AWS Global Accelerator:**
  - Improve global application availability and performance using the AWS global network

### 11.4. Amazon Route 53 Overview

- **Route 53 features are (non exhaustive list): Domain Registration, DNS, Health Checks, Routing Policy**
- Route53 is a Managed DNS (Domain Name System)
- DNS is a collection of rules and records which helps clients understand how to reach a server through URLs.
- In AWS, the most common records are:
  - www.google.com => 12.34.56.78 == A record (IPv4)
  - www.google.com => 2001:0db8:85a3:0000:0000:8a2e:0370:7334 == AAAA IPv6
  - search.google.com => www.google.com == CNAME: hostname to hostname
  - example.com => AWS resource == Alias (ex: ELB, CloudFront, S3, RDS, etc...)

#### 11.4.1. Route 53 policies

- **Weighted Routing Policy is used to route traffic to multiple resources in proportions that you specify.**

### 11.5. AWS CloudFront

- **CloudFront uses Edge Location to cache content, and therefore bring more of your content closer to your viewers to improve read performance.**
- **You can use AWS WAF web access control lists (web ACLs) to help minimize the effects of a distributed denial of service (DDoS) attack. For additional protection against DDoS attacks, AWS also provides AWS Shield Standard and AWS Shield Advanced.**
- Content Delivery Network (CDN)
- Improves read performance, content is cached at the edge
- Improves users experience
- 216 Point of Presence globally (edge locations)
- DDoS protection (because worldwide), integration with Shield, AWS Web Application Firewall

### 11.6. CloudFront - Origins

- S3 bucket
  - For distributing files and caching them at the edge
  - Enhanced security with CloudFront Origin Access Identity (OAI)
  - CloudFront can be used as an ingress (to upload files to S3)
- Custom Origin (HTTP)
  - Application Load Balancer
  - EC2 instance
  - S3 website (must first enable the bucket as a static S3 website)
  - Any HTTP backend you want

### 11.7. CloudFront vs S3 Cross Region Replication

- CloudFront:
  - Global Edge network.
  - Files are cached for a TTL (maybe a day).
  - Great for static content that must be available everywhere.
- S3 Cross Region Replication:
  - Must be setup for each region you want replication to happen.
  - Files are updated in near real-time.
  - Read only.
  - Great for dynamic content that needs to be available at low-latency in few regions.

### 11.8. S3 Transfer Acceleration

- **Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront's globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.**
- Increase transfer speed by transferring file to an AWS edge location which will forward the data to the S3 bucket in the target region.

### 11.9. AWS Global Accelerator

- Improve global application availability and performance using the AWS global network.
- Leverage the AWS internal network to optimize the route to your application (60% improvement).
- 2 Anycast IP are created for your application and traffic is sent through Edge Locations.
- The Edge locations send the traffic to your application.

### 11.10. AWS Global Accelerator vs CloudFront

- They both use the AWS global network and its edge locations around the world.
- Both services integrate with AWS Shield for DDoS protection.
- CloudFront - Content Delivery Network:
  - Improves performance for your cacheable content (such as images and videos).
  - Content is served at the edge.
- Global Accelerator:
  - No caching, proxying packets at the edge to applications running in one or more AWS Regions.
  - Improves performance for a wide range of applications over TCP or UDP.
  - Good for HTTP use cases that require static IP addresses.
  - Good for HTTP use cases that required deterministic, fast regional failover.

### 11.11. AWS Outposts

- Hybrid Cloud: businesses that keep an on-premises infrastructure alongside a cloud infrastructure.
- Therefore, two ways of dealing with IT systems:
  - One for the AWS cloud (using the AWS console, CLI, and AWS APIs).
  - One for their on-premises infrastructure.
- AWS Outposts are "server racks" that offers the same AWS infrastructure, services, APIs & tools to build your own applications on-premises just as in the cloud.
- AWS will setup and manage "Outposts Racks" within your on-premises infrastructure and you can start leveraging AWS services on-premises.
- You are responsible for the Outposts Rack physical security.
- Benefits:
  - Low-latency access to on-premises systems
  - Local data processing
  - Data residency
  - Easier migration from on-premises to the cloud
  - Fully managed service
- Some services that work on Outposts:
  - Amazon EC2
  - Amazon EBS
  - Amazon S3
  - Amazon EKS
  - Amazon ECS
  - Amazon RDS
  - Amazon EMR

### 11.12. AWS WaveLength

- **AWS Wavelength is an AWS Infrastructure offering optimized for mobile edge computing applications. Wavelength combines the high bandwidth and ultra-low latency of 5G networks with AWS compute and storage services to enable developers to innovate and build a whole new class of applications.**
- WaveLength Zones are infrastructure deployments embedded within the telecommunications providers datacenters at the edge of the 5G networks.
- Brings AWS services to the edge of the 5G networks.
- Example: EC2, EBS, VPC...
- Ultra-low latency applications through 5G networks.
- Traffic doesn't leave the Communication Service Provider's (CSP) network.
- High-bandwidth and secure connection to the parent AWS Region.
- No additional charges or service agreements.
- Use cases: Smart Cities, ML-assisted diagnostics, Connected Vehicles, Interactive Live Video Streams, AR/VR, Real-time Gaming, ...

### 11.13. AWS Local Zones

- Places AWS compute, storage, database, and other selected AWS services closer to end users to run latency-sensitive applications
- Extend your VPC to more locations - "Extension of an AWS Region"
- Compatible with EC2, RDS, ECS, EBS, ElastiCache, Direct Connect ...
- Example:
  - AWS Region: N. Virginia (us-east-1)
  - AWS Local Zones: Boston, Chicago, Dallas, Houston, Miami, ...

### 11.14. Global Applications Architecture

- Single Region, Single AZ.
- Single Region, Multi AZ.
- Multi Region, Active-Passive.
- Multi Region, Active-Active.

### 11.15. Global Applications in AWS - Summary

- Global DNS: Route 53
  - Great to route users to the closest deployment with least latency.
  - Great for disaster recovery strategies.
- Global Content Delivery Network (CDN): CloudFront
  - Replicate part of your application to AWS Edge Locations - decrease latency.
  - Cache common requests - improved user experience and decreased latency.
- S3 Transfer Acceleration
  - Accelerate global uploads & downloads into Amazon S3.
- AWS Global Accelerator
  - Improve global application availability and performance using the AWS global network.

### 11.16. Global Applications in AWS - Summary

- AWS Outposts
  - Deploy Outposts Racks in your own Data Centers to extend AWS services
- AWS WaveLength
  - Brings AWS services to the edge of the 5G networks
  - Ultra-low latency applications
- AWS Local Zones
  - Bring AWS resources (compute, database, storage, ...) closer to your users
  - Good for latency-sensitive applications

## 12. Cloud Integration

- When we start deploying multiple applications, they will inevitably need to communicate with one another.
- There are two patterns of application communication:
  1. Synchronous communications (application to application).
  2. Asynchronous / Event based (application to queue to application).
- Synchronous between applications can be problematic if there are sudden spikes of traffic.
- What if you need to suddenly encode 1000 videos but usually it's 10?
- In that case, it's better to decouple your applications:
  - using SQS: queue model.
  - using SNS: pub/sub model.
  - using Kinesis: real-time data streaming model.
- These services can scale independently from our application!

### 12.1. Amazon SQS - Standard Queue

- Oldest AWS offering (over 10 years old).
- Fully managed service (~serverless), use to decouple applications.
- Scales from 1 message per second to 10,000s per second.
- Default retention of messages: 4 days, maximum of 14 days.
- No limit to how many messages can be in the queue.
- Messages are deleted after they're read by consumers.
- Low latency (<10 ms on publish and receive).
- Consumers share the work to read messages & scale horizontally.

### 12.2. Amazon Kinesis

- **Amazon Kinesis makes it easy to collect, process, and analyze real-time, streaming data so you can get timely insights and react quickly to new information. Kinesis offers four services: Data Firehose, Data Analytics, Data Streams, Video Streams.**
- Kinesis = real-time big data streaming.
- Managed service to collect, process, and analyze real-time streaming data at any scale.
- Kinesis Data Streams: low latency streaming to ingest data at scale from hundreds of thousands of sources.
- Kinesis Data Firehose: load streams into S3, Redshift, ElasticSearch, etc...
- Kinesis Data Analytics: perform real-time analytics on streams using SQL.
- Kinesis Video Streams: monitor real-time video streams for analytics or ML.

### 12.3. Amazon SNS

- **Is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications. It uses a push-based system.**
- **Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. It uses a pull-based system.**
- The "event publishers" only sends message to one SNS topic.
- As many "event subscribers" as we want to listen to the SNS topic notifications.
- Each subscriber to the topic will get all the messages.
- Up to 12,500,000 subscriptions per topic, 100,000 topics limit.

### 12.4. Amazon MQ

- **Amazon MQ is a managed message broker service for Apache ActiveMQ and RabbitMQ that makes it easy to set up and operate message brokers in the cloud.**
- SQS, SNS are "cloud-native" services, and they're using proprietary protocols from AWS.
- Traditional applications running from on-premise may use open protocols such as: MQTT, AMQP, STOMP, Openwire, WSS.
- When migrating to the cloud, instead of re-engineering the application to use SQS and SNS, we can use Amazon MQ.
- Amazon MQ = managed Apache ActiveMQ.
- Amazon MQ doesn't "scale" as much as SQS / SNS.
- Amazon MQ runs on a dedicated machine (not serverless).
- Amazon MQ has both queue feature (SQS) and topic features (SNS).

### 12.5. Integration - Summary

- SQS:
  - Queue service in AWS.
  - Multiple Producers, messages are kept up to 14 days.
  - Multiple Consumers share the read and delete messages when done.
  - Used to decouple applications in AWS.
- SNS:
  - Notification service in AWS.
  - Subscribers: Email, Lambda, SQS, HTTP, Mobile...
  - Multiple Subscribers, send all messages to all of them.
  - No message retention.
- Kinesis: real-time data streaming, persistence and analysis.
- Amazon MQ: managed Apache MQ in the cloud (MQTT, AMQP protocols).
- **When using SQS or SNS, you apply the "decouple your applications" principle. This means that IT systems should be designed in a way that reduces interdependencies—a change or a failure in one component should not cascade to other components.**

## 13. Cloud Monitoring

### 13.1. Amazon CloudWatch Metrics

- **Amazon CloudWatch is a monitoring service for AWS cloud resources and the applications you run on AWS. You can use Amazon CloudWatch to collect and track metrics, collect and monitor log files, and set alarms.**
- CloudWatch provides metrics for every services in AWS.
- **Metric** is a variable to monitor (CPUUtilization, NetworkIn...).
- Metrics have **timestamps**.
- Can create **CloudWatch dashboards** of metrics.

#### 13.1.1. Important Metrics

- EC2 instances: CPU Utilization, Status Checks, Network (not RAM).
  - Default metrics every 5 minutes.
  - Option for Detailed Monitoring ($$$): metrics every 1 minute.
- EBS volumes: Disk Read/Writes.
- S3 buckets: BucketSizeBytes, NumberOfObjects, AllRequests.
- Billing:Total Estimated Charge (only in us-east-1).
- Service Limits: how much you've been using a service API.
- Custom metrics: push your own metrics.

### 13.2. Amazon CloudWatch Alarms

- **The CloudWatch Alarms feature allows you to watch CloudWatch metrics and to receive notifications when the metrics fall outside of the levels (high or low thresholds) that you configure.**
- Alarms are used to trigger notifications for any metric
- Alarms actions...
  - Auto Scaling: increase or decrease EC2 instances "desired" count
  - EC2 Actions: stop, terminate, reboot or recover an EC2 instance
  - SNS notifications: send a notification into an SNS topic
- Various options (sampling, %, max, min, etc...)
- Can choose the period on which to evaluate an alarm
- Example: create a billing alarm on the CloudWatch Billing metric
- Alarm States: OK. INSUFFICIENT_DATA, ALARM

### 13.3. Amazon CloudWatch Logs

- CloudWatch Logs can collect log from:
  - Elastic Beanstalk: collection of logs from application.
  - ECS: collection from containers.
  - AWS Lambda: collection from function logs.
  - CloudTrail based on filter.
  - CloudWatch log agents: on EC2 machines or on-premises servers.
  - Route53: Log DNS queries.
- Enables real-time monitoring of logs.
- Adjustable CloudWatch Logs retention.

### 13.4. CloudWatch Logs for EC2

- By default, no logs from your EC2 instance will go to CloudWatch.
- You need to run a **CloudWatch agent** on EC2 to push the log files you want.
- Make sure IAM permissions are correct.
- **The CloudWatch log agent can be setup on-premises too**.

### 13.5. Amazon CloudWatch Events

- Schedule: Cron jobs (scheduled scripts).
- Event Pattern: Event rules to react to a service doing something.
- Trigger Lambda functions, send SQS/SNS messages...

### 13.6. Amazon EventBridge

- EventBridge is the next evolution of CloudWatch Events.
- **Default event bus**: generated by AWS services (CloudWatch Events).
- **Partner event bus**: receive events from SaaS service or applications (Zendesk, DataDog, Segment, Auth0...).
- Custom Event buses: for your own applications.
- Schema Registry: model event schema.
- EventBridge has a different name to mark the new capabilities.
- The CloudWatch Events name will be replaced with EventBridge.

### 13.7. AWS CloudTrail

- **Is a web service that records activity made on your account and delivers log files to your Amazon S3 bucket. AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account.**
- **Can record the history of events/API calls made within you AWS account, which will help determine who or what deleted the resource. You should investigate it first.**
- Provides governance, compliance and audit for your AWS Account.
- CloudTrail is enabled by default!
- Get an history of events / API calls made within your AWS Account by:
  - Console.
  - SDK.
  - CLI.
  - AWS Services.
- Can put logs from CloudTrail into CloudWatch Logs or S3.
- A trail can be applied to All Regions (default) or a single Region.
- If a resource is deleted in AWS, investigate CloudTrail first!

### 13.8. CloudTrail Events

- Management Events:
  - Operations that are performed on resources in your AWS account
  - Examples:
    - Configuring security (IAM AttachRolePolicy)
    - Configuring rules for routing data (Amazon EC2 CreateSubnet)
    - Setting up logging (AWS CloudTrail CreateTrail)
  - **By default, trails are configured to log management events**.
  - Can separate Read Events (that don't modify resources) from Write Events (that may modify resources)
- Data Events:
  - By default, data events are not logged (because high volume operations)
  - Amazon S3 object-level activity (ex: GetObject, DeleteObject, PutObject): can separate Read and Write Events
  - AWS Lambda function execution activity (the Invoke API)

#### 13.8.1. CloudTrail Insights Events

- **AWS CloudTrail Insights helps AWS users identify and respond to unusual activity associated with write API calls by continuously analyzing CloudTrail management events.**
- Enable **CloudTrail Insights to detect unusual activity** in your account:
  - Inaccurate resource provisioning.
  - Hitting service limits.
  - Bursts of AWS IAM actions.
  - Gaps in periodic maintenance activity.
- CloudTrail Insights analyzes normal management events to create a baseline.
- And then **continuously analyzes write events to detect unusual patterns**.
  - Anomalies appear in the CloudTrail console.
  - Event is sent to Amazon S3.
  - An EventBridge event is generated (for automation needs).

#### 13.8.2. CloudTrail Events Retention

- Events are stored for 90 days in CloudTrail.
- To keep events beyond this period, log them to S3 and use Athena.

### 13.9. AWS X-Ray

- **AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture.**
- Debugging in Production, the good old way:
  - Test locally.
  - Add log statements everywhere.
  - Re-deploy in production.
- Log formats differ across applications and log analysis is hard.
- Debugging: one big monolith "easy", distributed services "hard".
- No common views of your entire architecture.

#### 13.9.1. AWS X-Ray advantages

- Troubleshooting performance (bottlenecks)
- Understand dependencies in a microservice architecture
- Pinpoint service issues
- Review request behavior
- Find errors and exceptions
- Are we meeting time SLA?
- Where I am throttled?
- Identify users that are impacted

### 13.10. Amazon CodeGuru

- **Amazon CodeGuru is a developer tool that provides intelligent recommendations to improve code quality and identify an application's most expensive lines of code.**
- An ML-powered service for **automated code reviews** and **application performance recommendations**.
- Provides two functionalities
  - **CodeGuru Reviewer:** automated code reviews for static code analysis (development)
  - **CodeGuru Profiler:** visibility/recommendations about application performance during runtime (production)

### 13.11. Amazon CodeGuru Reviewer

- Identify critical issues, security vulnerabilities, and hard-to-find bugs.
- Example: common coding best practices, resource leaks, security detection, input validation.
- Uses Machine Learning and automated reasoning.
- Hard-learned lessons across millions of code reviews on 1000s of open-source and Amazon repositories.
- Supports Java and Python.
- Integrates with GitHub, Bitbucket, and AWS CodeCommit.

#### 13.11.1. Amazon CodeGuru Profiler

- Helps understand the runtime behavior of your application.
- Example: identify if your application is consuming excessive CPU capacity on a logging routine.
- Features:
  - Identify and remove code inefficiencies.
  - Improve application performance (e.g., reduce CPU utilization).
  - Decrease compute costs.
  - Provides heap summary (identify which objects using up memory).
  - Anomaly Detection.
- Support applications running on AWS or on-premise.
- Minimal overhead on application.

### 13.12. AWS Status - Service Health Dashboard

- Shows all regions, all services health
- Shows historical information for each day
- Has an RSS feed you can subscribe to
- https://status.aws.amazon.com/

### 13.13. AWS Personal Health Dashboard

- AWS Personal Health Dashboard provides **alerts and remediation guidance** when AWS is experiencing **events that may impact you**.
- While the Service Health Dashboard displays the general status of AWS services, Personal Health Dashboard gives you a **personalized view into the performance and availability of the AWS services underlying your AWS resources**.
- The dashboard displays **relevant and timely information** to help you manage events in progress and **provides proactive** notification to help you plan for **scheduled activities**.
- Global service https://phd.aws.amazon.com/
- Shows how AWS outages directly impact you & your AWS resources.
- Alert, remediation, proactive, scheduled activities.

### 13.14. Monitoring Summary

- CloudWatch:
  - Metrics: monitor the performance of AWS services and billing metrics.
  - Alarms: automate notification, perform EC2 action, notify to SNS based on metric.
  - Logs: collect log files from EC2 instances, servers, Lambda functions...
  - Events (or EventBridge): react to events in AWS, or trigger a rule on a schedule.
- CloudTrail: audit API calls made within your AWS account.
- CloudTrail Insights: automated analysis of your CloudTrail Events.
- X-Ray: trace requests made through your distributed applications.
- Service Health Dashboard: status of all AWS services across all regions.
- Personal Health Dashboard: AWS events that impact your infrastructure.
- Amazon CodeGuru: automated code reviews and application performance recommendation.

## 14. VPC

### 14.1. VPC - Crash Course

- At the AWS Certified Cloud Practitioner Level, you should know about:
  - VPC, Subnets, Internet Gateways & NAT Gateways.
  - Security Groups, Network ACL (NACL), VPC Flow Logs.
  - VPC Peering, VPC Endpoints.
  - Site to Site VPN & Direct Connect.
  - Transit Gateway.
- We'll have a look at the "default VPC" (created by default by AWS for you).

### 14.2. VPC & Subnets Primer

- **A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your VPC.**
- **VPC - Virtual Private Cloud:** private network to deploy your resources (regional resource).
- **Subnets** allow you to partition your network inside your VPC (Availability Zone resource).
- A **public subnet** is a subnet that is accessible from the internet.
- A **private subnet** is a subnet that is not accessible from the internet.
- To define access to the internet and between subnets, we use Route Tables.

### 14.3. Internet Gateway & NAT Gateways

- **NAT Gateways allow your instances in your private subnets to access the Internet while remaining private, and are managed by AWS.**
- **Internet Gateways** helps our VPC instances connect with the internet.
- Public Subnets have a route to the internet gateway.
- **NAT Gateways** (AWS-managed)
- **NAT Instances** (self-managed) allow your instances in your **Private Subnets** to access the internet while remaining private.
  - **NAT Instances allow your instances in your private subnets to access the Internet while remaining private, but are managed by you.**

### 14.4. Network ACL & Security Groups

- **A network access control list (NACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. They have both ALLOW and DENY rules.**
  - **NACL (Network ACL):**
    - A firewall which controls traffic from and to subnet.
    - Can have ALLOW and DENY rules.
    - Are attached at the **Subnet** level.
    - Rules only include IP addresses.
- **Security Groups:**
  - A firewall that controls traffic to and from **an ENI / an EC2 Instance**.
  - Can have only ALLOW rules.
  - Rules include IP addresses and other security groups.

### 14.5. Network ACLs vs Security Groups

| Security group                                                                                                                                               | Network ACL                                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Operates at the instance level                                                                                                                               | Operates at the subnet level                                                                                                                                                           |
| Supports allow rules only                                                                                                                                    | Supports allow rules and deny rules                                                                                                                                                    |
| Is stateful: Return traffic is automatically allowed, regardless of any rules                                                                                | Is stateless: Return traffic must be explicitly allowed by rules                                                                                                                       |
| We evaluate all rules before deciding whether to allow traffic                                                                                               | We process rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic                                                                              |
| Applies to an instance only if someone specifies the security group when launching the instance, or associates the security group with the instance later on | Automatically applies to all instances in the subnets that it's associated with (therefore, it provides an additional layer of defense if the security group rules are too permissive) |

- https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Security.html

### 14.6. VPC Flow Logs

- Capture information about IP traffic going into your interfaces:
  - **VPC Flow** Logs.
  - **Subnet** Flow Logs.
  - **Elastic Network Interface** Flow Logs.
- Helps to monitor & troubleshoot connectivity issues. Example:
  - Subnets to internet.
  - Subnets to subnets.
  - Internet to subnets.
- Captures network information from AWS managed interfaces too: Elastic Load Balancers, ElastiCache, RDS, Aurora, etc...
- VPC Flow logs data can go to S3 / CloudWatch Logs.

### 14.7. VPC Peering

- Connect two VPC, privately using AWS' network.
- Make them behave as if they were in the same network.
- Must not have overlapping CIDR (IP address range).
- VPC Peering connection is not transitive (must be established for each VPC that need to communicate with one another).

### 14.8. VPC Endpoints

- Endpoints allow you to connect to AWS Services **using a private network** instead of the public www network.
- This gives you enhanced security and lower latency to access AWS services.
- VPC Endpoint **Gateway**: S3 & DynamoDB.
- VPC Endpoint **Interface**: the rest.

### 14.9. Site to Site VPN & Direct Connect

- **Site to Site VPN:**
  - Connect an on-premises VPN to AWS.
  - The connection is automatically encrypted.
  - Goes over the public internet.
- **AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated private network connection from your premises to AWS.**
  - **Direct Connect (DX):**
    - Establish a physical connection between on-premises and AWS.
    - The connection is private, secure and fast.
    - Goes over a private network.
    - Takes at least a month to establish.

### 14.10. Site-to-Site VPN

- On-premises: must use a **Customer Gateway** (CGW)
- AWS: must use a **Virtual Private Gateway** (VGW)

### 14.11. Transit Gateway

- **Transit Gateway connects thousands of VPC and on-premises networks together in a single gateway.**
- For having transitive peering between thousands of VPC and on-premises, hub-and-spoke (star) connection.
- One single Gateway to provide this functionality.
- Works with Direct Connect Gateway, VPN connections.

### 14.12. VPC Closing Comments

- VPC: Virtual Private Cloud.
- Subnets:Tied to an AZ, network partition of the VPC.
- Internet Gateway: at the VPC level, provide Internet Access.
- NAT Gateway / Instances: give internet access to private subnets.
- NACL: Stateless, subnet rules for inbound and outbound.
- Security Groups: Stateful, operate at the EC2 instance level or ENI.
- VPC Peering: Connect two VPC with non overlapping IP ranges, nontransitive.
- VPC Endpoints: Provide private access to AWS Services within VPC.
- VPC Flow Logs: network traffic logs.
- Site to Site VPN: VPN over public internet between on-premises DC and AWS.
- Direct Connect: direct private connection to AWS.
- Transit Gateway: Connect thousands of VPC and on-premises networks together.

## 15. Security & Compliance

### 15.1. AWS Shared Responsibility Model

- AWS responsibility - Security of the Cloud
  - Protecting infrastructure (hardware, software, facilities, and networking) that runs all the AWS services.
  - Managed services like S3, DynamoDB, RDS, etc.
- Customer responsibility - Security in the Cloud
  - For EC2 instance, customer is responsible for management of the guest OS (including security patches and updates), firewall & network configuration, IAM.
  - Encrypting application data.
- Shared controls:
  - **AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications. Shared Controls also includes Configuration Management, and Awareness and Training.**
  - Patch Management, Configuration Management, Awareness & Training.

#### 15.1.1. Example, for RDS

- AWS responsibility:
  - Manage the underlying EC2 instance, disable SSH access.
  - Automated DB patching.
  - Automated OS patching.
  - Audit the underlying instance and disks & guarantee it functions.
- Your responsibility:
  - Check the ports / IP / security group inbound rules in DB's SG.
  - In-database user creation and permissions.
  - Creating a database with or without public access.
  - Ensure parameter groups or DB is configured to only allow SSL connections.
  - Database encryption setting.

#### 15.1.2. Example, for S3

- AWS responsibility:
  - Guarantee you get unlimited storage.
  - Guarantee you get encryption.
  - Ensure separation of the data between different customers.
  - Ensure AWS employees can't access your data.
- Your responsibility:
  - Bucket configuration.
  - Bucket policy / public setting.
  - IAM user and roles.
  - Enabling encryption.

### 15.2. DDOS Protection on AWS

- DDOS = Distributed Denial-of-Service
- **AWS Shield Standard:** protects against DDOS attack for your website and applications, for all customers at no additional costs
- **AWS Shield Advanced:** 24/7 premium DDoS protection
- **AWS WAF:** Filter specific requests based on rules
- **CloudFront and Route 53:**
  - Availability protection using global edge network
  - Combined with AWS Shield, provides attack mitigation at the edge
- Be ready to scale - leverage **AWS Auto Scaling**

### 15.3. AWS Shield

- **AWS Shield Standard:**
  - Free service that is activated for every AWS customer.
  - Provides protection from attacks such as SYN/UDP Floods, Reflection attacks and other layer 3/layer 4 attacks.
- **AWS Shield Advanced:**
  - Optional DDoS mitigation service ($3,000 per month per organization).
  - Protect against more sophisticated attack on Amazon EC2, Elastic Load Balancing (ELB), Amazon CloudFront, AWS Global Accelerator, and Route 53.
  - 24/7 access to AWS DDoS response team (DRP).
  - Protect against higher fees during usage spikes due to DDoS.

### 15.4. AWS WAF - Web Application Firewall

- **AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources.**
- Protects your web applications from common web exploits (Layer 7).
- **Layer 7 is HTTP** (vs Layer 4 is TCP).
- Deploy on **Application Load Balancer, API Gateway, CloudFront**.
- Define Web ACL (Web Access Control List):
  - Rules can include IP addresses, HTTP headers, HTTP body, or URI strings.
  - Protects from common attack - **SQL injection** and **Cross-Site Scripting (XSS)**.
  - Size constraints, **geo-match (block countries)**.
  - Rate-based rules (to count occurrences of events) - for DDoS protection.

### 15.5. Penetration Testing on AWS Cloud

- AWS customers are welcome to carry out security assessments or penetration tests against their AWS infrastructure **without prior approval for 8 services**:
  - Amazon EC2 instances, NAT Gateways, and Elastic Load Balancers.
  - Amazon RDS.
  - Amazon CloudFront.
  - Amazon Aurora.
  - Amazon API Gateways.
  - AWS Lambda and Lambda Edge functions.
  - Amazon Lightsail resources.
  - Amazon Elastic Beanstalk environments.
- List can increase over time...
- **Prohibited Activities**
  - DNS zone walking via Amazon Route 53 Hosted Zones.
  - Denial of Service (DoS), Distributed Denial of Service (DDoS), Simulated DoS, Simulated DDoS.
  - Port flooding.
  - Protocol flooding.
  - Request flooding (login request flooding, API request flooding).
- For any other simulated events, contact aws-security-simulated-event@amazon.com.
- Read more: https://aws.amazon.com/security/penetration-testing/.

### 15.6. Data at rest vs. Data in transit

- **At rest:** data stored or archived on a device.
  - On a hard disk, on a RDS instance, in S3 Glacier Deep Archive, etc.
- **In transit (in motion):** data being moved from one location to another.
  - Transfer from on-premises to AWS, EC2 to DynamoDB, etc.
  - Means data transferred on the network.
- We want to encrypt data in both states to protect it!
- For this we leverage **encryption keys**.

### 15.7. AWS KMS (Key Management Service)

- Anytime you hear "encryption" for an AWS service, it's most likely KMS.
- KMS = **AWS manages the encryption keys for us**.
- **Encryption Opt-in:**
  - EBS volumes: encrypt volumes.
  - S3 buckets: Server-side encryption of objects.
  - Redshift database: encryption of data.
  - RDS database: encryption of data.
  - EFS drives: encryption of data.
- **Encryption Automatically enabled:**
  - CloudTrail Logs.
  - S3 Glacier.
  - Storage Gateway.

### 15.8. CloudHSM

- KMS => AWS manages the software for encryption.
- CloudHSM => AWS provisions encryption hardware.
- Dedicated Hardware (HSM = Hardware Security Module).
- You manage your own encryption keys entirely (not AWS).
- HSM device is tamper resistant, FIPS 140-2 Level 3 compliance.

### 15.9. Types of CMK (Customer Master Keys)

- **Customer Managed CMK:**
  - Create, manage and used by the customer, can enable or disable.
  - Possibility of rotation policy (new key generated every year, old key preserved).
  - Possibility to bring-your-own-key.
- **AWS managed CMK:**
  - Created, managed and used on the customer's behalf by AWS.
  - Used by AWS services (aws/s3, aws/ebs, aws/redshift).
- **AWS owned CMK:**
  - Collection of CMKs that an AWS service owns and manages to use in multiple accounts.
  - AWS can use those to protect resources in your account (but you can't view the keys).
- **CloudHSM Keys (custom keystore):**
  - Keys generated from your own CloudHSM hardware device.
  - Cryptographic operations are performed within the CloudHSM cluster.

### 15.10. AWS Certificate Manager (ACM)

- **AWS Certificate Manager is a service that lets you easily provision, manage, and deploy public and private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates for use with AWS services and your internal connected resources.**
- Used to provide in-flight encryption for websites (HTTPS).
- Supports both public and private TLS certificates.
- Free of charge for public TLS certificates.
- Automatic TLS certificate renewal.
- Integrations with (load TLS certificates on):
  - Elastic Load Balancers.
  - CloudFront Distributions.
  - APIs on API Gateway Auto Scaling group.

### 15.11. AWS Secrets Manager

- Newer service, meant for storing secrets.
- Capability to force **rotation of secrets** every X days.
- Automate generation of secrets on rotation (uses Lambda).
- Integration with Amazon RDS (MySQL, PostgreSQL, Aurora).
- Secrets are encrypted using KMS.
- Mostly meant for RDS integration.

### 15.12. AWS Artifact (not really a service)

- **AWS Artifact is your go-to, central resource for compliance-related information that matters to you.**
- Portal that provides customers with on-demand access to AWS compliance documentation and AWS agreements.
- **Artifact Reports** - Allows you to download AWS security and compliance documents from third-party auditors, like AWS ISO certifications, Payment Card Industry (PCI), and System and Organization Control (SOC) reports.
- **Artifact Agreements** - Allows you to review, accept, and track the status of AWS agreements such as the Business Associate Addendum (BAA) or the Health Insurance Portability and Accountability Act (HIPAA) for an individual account or in your organization.
- Can be used to support internal audit or compliance.

### 15.13. Amazon GuardDuty

- **Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts and workloads.**
- Intelligent Threat discovery to Protect AWS Account.
- Uses Machine Learning algorithms, anomaly detection, 3rd party data.
- One click to enable (30 days trial), no need to install software.
- Input data includes:
  - CloudTrail Events Logs - unusual API calls, unauthorized deployments.
    - CloudTrail Management Events - create VPC subnet, create trail, ...
    - CloudTrail S3 Data Events - get object, list objects, delete object, ...
  - VPC Flow Logs - unusual internal traffic, unusual IP address.
  - DNS Logs - compromised EC2 instances sending encoded data within DNS queries.
  - Kubernetes Audit Logs - suspicious activities and potential EKS cluster compromises.
- Can setup CloudWatch Event rules to be notified in case of findings.
- CloudWatch Events rules can target AWS Lambda or SNS.
- Can protect against CryptoCurrency attacks (has a dedicated "finding" for it).

### 15.14. Amazon Inspector

- **Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. It helps you test the network accessibility of your Amazon EC2 instances and the security state of your applications running on the instances.**
- **Automated Security Assessments**.
- **For EC2 instances:**
  - Leveraging the AWS System Manager (SSM) agent.
  - Analyze against unintended network accessibility.
  - Analyze the running OS against known vulnerabilities.
- **For Containers push to Amazon ECR:**
  - Assessment of containers as they are pushed.
- Reporting & integration with AWS Security Hub.
- Send findings to Amazon Event Bridge.

#### 15.14.1. What does AWS Inspector evaluate?

- **Only for EC2 instances and container infrastructure**.
- Continuous scanning of the infrastructure, only when needed.
- Package vulnerabilities (EC2 & ECR) - database of CVE.
- Network reachability (EC2).
- A risk score is associated with all vulnerabilities for prioritization.

### 15.15. AWS Config

- **AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources.**
- Helps with **auditing and recording compliance of your AWS resources**.
- Helps record configurations and changes over time.
- Possibility of storing the configuration data into S3 (analyzed by Athena).
- Questions that can be solved by AWS Config:
  - Is there unrestricted SSH access to my security groups?
  - Do my buckets have any public access?
  - How has my ALB configuration changed over time?
- You can receive alerts (SNS notifications) for any changes.
- AWS Config is a per-region service.
- Can be aggregated across regions and accounts.

### 15.16. Amazon Macie

- Amazon Macie is a fully managed data security and data privacy service that uses **machine learning and pattern matching to discover and protect your sensitive data in AWS**.
- Macie helps identify and alert you to **sensitive data, such as personally identifiable information (PII)**.

### 15.17. AWS Security Hub

- **AWS Security Hub provides you with a comprehensive view of your security state within AWS and your compliance with security standards and best practices.**
- Central security tool to manage security across several AWS accounts and automate security checks.
- Integrated dashboards showing current security and compliance status to quickly take actions.
- Automatically aggregates alerts in predefined or personal findings formats from various AWS services & AWS partner tools:
  - GuardDuty.
  - Inspector.
  - Macie.
  - IAM Access Analyzer.
  - AWS Systems Manager.
  - AWS Firewall Manager.
  - AWS Partner Network Solutions.
- Must first enable the AWS Config Service.

### 15.18. Amazon Detective

- Amazon Detective **analyzes, investigates, and quickly identifies the root cause of security issues or suspicious activities (using ML and graphs)**.
- GuardDuty, Macie, and Security Hub are used to identify potential security issues, or findings.
- Sometimes security findings require deeper analysis to isolate the root cause and take action - it's a complex process.
- Automatically collects and processes events from VPC Flow Logs, CloudTrail, GuardDuty and create a unified view.
- Produces visualizations with details and context to get to the root cause.

### 15.19. AWS Abuse

- **Report suspected AWS resources used for abusive or illegal purposes**.
- Abusive & prohibited behaviors are:
  - **Spam** - receving undesired emails from AWS-owned IP address, websites & forums spammed by AWS resources.
  - **Port scanning**- sending packets to your ports to discover the unsecured ones.
  - **DoS or DDoS attacks** - AWS-owned IP addresses attempting to overwhlem or crash your servers/softwares.
  - **Intrusion attempts** - logging in on your resources.
  - **Hosting objectionable** or copyrighted content - distributing illegal or copyrighted content without consent.
  - **Distributing malware** - AWS resources distributing softwares to harm computers or machines.
- Contact the AWS Abuse team: AWS abuse form, or abuse@amazonaws.com.

### 15.20. Root user privileges

- Root user = Account Owner (created when the account is created).
- Has complete access to all AWS services and resources.
- **Lock away your AWS account root user access keys!**.
- Do not use the root account for everyday tasks, even administrative tasks.
- Actions that can be performed only by the root user:
  - Change account settings (account name, email address, root user password, root user access keys).
  - View certain tax invoices.
  - Close your AWS account.
  - Restore IAM user permissions.
  - Change or cancel your AWS Support plan.
  - Register as a seller in the Reserved Instance Marketplace.
  - Configure an Amazon S3 bucket to enable MFA.
  - Edit or delete an Amazon S3 bucket policy that includes an invalid VPC ID or VPC endpoint ID.
  - Sign up for GovCloud.

### 15.21. Summary: Security & Compliance

- Shared Responsibility on AWS
- Shield: Automatic DDoS Protection + 24/7 support for advanced
- WAF: Firewall to filter incoming requests based on rules
- KMS: Encryption keys managed by AWS
- CloudHSM: Hardware encryption, we manage encryption keys
- AWS Certificate Manager: provision, manage, and deploy SSL/TLS Certificates
- Artifact: Get access to compliance reports such as PCI, ISO, etc...
- GuardDuty: Find malicious behavior with VPC, DNS & CloudTrail Logs
- Inspector: For EC2 only, install agent and find vulnerabilities
- Config: Track config changes and compliance against rules
- Macie: Find sensitive data (ex: PII data) in Amazon S3 buckets
- CloudTrail: Track API calls made by users within account
- AWS Security Hub: gather security findings from multiple AWS accounts
- Amazon Detective: find the root cause of security issues or suspicious activities
- AWS Abuse: Report AWS resources used for abusive or illegal purposes
- Root user privileges:
  - Change account settings
  - Close your AWS account
  - Change or cancel your AWS Support plan
  - Register as a seller in the Reserved Instance Marketplace

## 16. Machine Learning

### 16.1. Amazon Rekognition

- **Amazon Rekognition makes it easy to add image and video analysis to your applications using proven, highly scalable, deep learning technology that requires no machine learning expertise to use.**
- Find objects, people, text, scenes in images and videos using ML.
- Facial analysis and facial search to do user verification, people counting.
- Create a database of "familiar faces" or compare against celebrities.
- Use cases:
  - Labeling.
  - Content Moderation.
  - Text Detection.
  - Face Detection and Analysis (gender, age range, emotions...).
  - Face Search and Verification.
  - Celebrity Recognition.
  - Pathing (ex: for sports game analysis).

### 16.2. Amazon Transcribe

- **Amazon Transcribe is an AWS service that makes it easy for customers to convert speech-to-text.**
- Automatically convert speech to text.
- Uses a deep learning process called automatic speech recognition (ASR) to convert speech to text quickly and accurately.
- Use cases:
  - Transcribe customer service calls.
  - Automate closed captioning and subtitling.
  - Generate metadata for media assets to create a fully searchable archive.

### 16.3. Amazon Polly

- **Amazon Polly is a service that turns text into lifelike speech.**
- Turn text into lifelike speech using deep learning.
- Allowing you to create applications that talk.

### 16.4. Amazon Translate

- **Amazon Translate is a neural machine translation service that delivers fast, high-quality, and affordable language translation.**
- Natural and accurate **language translation**.
- Amazon Translate allows you to **localize content** - such as websites and applications - for **international users**, and to easily translate large volumes of text efficiently.

### 16.5. Amazon Lex & Connect

- **Amazon Lex is a service for building conversational interfaces into any application using voice and text. Lex provides the advanced deep learning functionalities of automatic speech recognition (ASR) for converting speech to text, and natural language understanding (NLU) to recognize the intent of the text, to enable you to build applications with highly engaging user experiences and lifelike conversational interactions.**
- **Amazon Lex:** (same technology that powers Alexa).
  - Automatic Speech Recognition (ASR) to convert speech to text.
  - Natural Language Understanding to recognize the intent of text, callers.
  - Helps build chatbots, call center bots.
- **Amazon Connect is a self-service, cloud-based contact center service that makes it easy for any business to deliver better customer service at lower cost. It does not provide speech-to-text conversion or natural language understanding.**
- **Amazon Connect:**
  - Receive calls, create contact flows, cloud-based virtual contact center.
  - Can integrate with other CRM systems or AWS.
  - No upfront payments, 80% cheaper than traditional contact center solutions.

### 16.6. Amazon Comprehend

- **Amazon Comprehend is a natural language processing (NLP) service that uses machine learning to find meaning and insights in text.**
- For **Natural Language Processing - NLP**.
- Fully managed and serverless service.
- Uses machine learning to find insights and relationships in text:
  - Language of the text.
  - Extracts key phrases, places, people, brands, or events.
  - Understands how positive or negative the text is.
  - Analyzes text using tokenization and parts of speech.
  - Automatically organizes a collection of text files by topic.
- Sample use cases:
  - Analyze customer interactions (emails) to find what leads to a positive or negative experience.
  - Create and groups articles by topics that Comprehend will uncover.

### 16.7. Amazon SageMaker

- **Amazon SageMaker is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning (ML) models quickly. SageMaker removes the heavy lifting from each step of the machine learning process to make it easier to develop high quality models.**
- Fully managed service for developers / data scientists to build ML models.
- Typically, difficult to do all the processes in one place + provision servers.
- Machine learning process (simplified): predicting your exam score.

### 16.8. Amazon Forecast

- Fully managed service that uses ML to deliver highly accurate forecasts.
- Example: predict the future sales of a raincoat.
- 50% more accurate than looking at the data itself.
- Reduce forecasting time from months to hours.
- Use cases: Product Demand Planning, Financial Planning, Resource Planning, ...

### 16.9. Amazon Kendra

- **Amazon Kendra is a highly accurate and easy to use enterprise search service that's powered by machine learning.**
- Fully managed **document search service** powered by Machine Learning.
- Extract answers from within a document (text, pdf, HTML, PowerPoint, MS Word, FAQs...).
- Natural language search capabilities.
- Learn from user interactions/feedback to promote preferred results **(Incremental Learning)**.
- Ability to manually fine-tune search results (importance of data, freshness, custom, ...).

### 16.10. Amazon Personalize

- **Amazon Personalize is a machine learning service that makes it easy for developers to create individualized recommendations for customers using their applications.**
- Fully managed ML-service to build apps with real-time personalized recommendations.
- Example: personalized product recommendations/re-ranking, customized direct marketing.
  - Example: User bought gardening tools, provide recommendations on the next one to buy.
- Same technology used by Amazon.com.
- Integrates into existing websites, applications, SMS, email marketing systems, ...
- Implement in days, not months (you don't need to build, train, and deploy ML solutions).
- Use cases: retail stores, media and entertainment...

### 16.11. AWS Machine Learning - Summary

- Rekognition: face detection, labeling, celebrity recognition.
- Transcribe: audio to text (ex: subtitles).
- Polly: text to audio.
- Translate: translations.
- Lex: build conversational bots - chatbots.
- Connect: cloud contact center.
- Comprehend: natural language processing.
- SageMaker: machine learning for every developer and data scientist.
- Forecast: build highly accurate forecasts.
- Kendra: ML-powered search engine.
- Personalize: real-time personalized recommendations.

## 17. Advanced Identity

### 17.1. AWS STS (SecurityToken Service)

- **AWS Security Token Service (AWS STS) is a web service that enables you to request temporary, limited-privilege credentials for AWS Identity and Access Management (IAM) users or for users that you authenticate (federated users).**
- Enables you to create temporary, limited- privileges credentials to access your AWS resources.
- Short-term credentials: you configure expiration period.
- Use cases:
  - Identity federation: manage user identities in external systems, and provide them with STS tokens to access AWS resources.
  - IAM Roles for cross/same account access.
  - IAM Roles for Amazon EC2: provide temporary credentials for EC2 instances to access AWS resources.

### 17.2. Amazon Cognito

- **Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily.**
- Identity for your Web and Mobile applications users (potentially millions).
- Instead of creating them an IAM user, you create a user in Cognito.

### 17.3. What is Microsoft Active Directory (AD)?

- Found on any Windows Server with AD Domain Services.
- Database of objects: User Accounts, Computers, Printers, File Shares, Security Groups.
- Centralized security management, create account, assign permissions.

#### 17.3.1. AWS Directory Services

- **AWS Directory Service makes it easy for you to setup and run directories in the AWS cloud, or connect your AWS resources with an existing on-premises Microsoft Active Directory.**
- **AWS Managed Microsoft AD:**
  - Create your own AD in AWS, manage users locally, supports MFA.
  - Establish "trust" connections with your on- premise AD.
- **AD Connector:**
  - Directory Gateway (proxy) to redirect to on- premise AD, supports MFA.
  - Users are managed on the on-premise AD.
- **Simple AD:**
  - AD-compatible managed directory on AWS.
  - Cannot be joined with on-premise AD.

### 17.4. AWS Organizations

- Organizations helps you to centrally manage billing; control access, compliance, and security; and share resources across your AWS accounts.

### 17.5. AWS Single Sign-On (SSO)

- Centrally manage Single Sign-On to access multiple accounts and 3rd-party business applications.
- Integrated with AWS Organizations.
- Supports SAML 2.0 markup.
- Integration with on-premise Active Directory.

### 17.6. Advanced Identity - Summary

- IAM:
  - Identity and Access Management inside your AWS account.
  - For users that you trust and belong to your company.
  - **IAM Roles are sets of permissions making AWS service requests, which will be used by AWS services, but they do not provide temporary security credentials.**
- Organizations: manage multiple AWS accounts.
- Security Token Service (STS): temporary, limited-privileges credentials to access AWS resources.
- Cognito: create a database of users for your mobile & web applications.
- Directory Services: integrate Microsoft Active Directory in AWS.
- Single Sign-On (SSO): one login for multiple AWS accounts & applications.

## 18. Other AWS Services

### 18.1. Amazon WorkSpaces

- **Amazon WorkSpaces is a fully managed, secure cloud desktop service. You can use Amazon WorkSpaces to provision either Windows or Linux desktops in just a few minutes and quickly scale to provide thousands of desktops to workers across the globe.**
- Managed Desktop as a Service (DaaS) solution to easily provision Windows or Linux desktops.
- Great to eliminate management of on-premise VDI (Virtual Desktop Infrastructure).
- Fast and quickly scalable to thousands of users.
- Secured data - integrates with KMS.
- Pay-as-you-go service with monthly or hourly rates.

### 18.2. Amazon AppStream 2.0

- **Amazon AppStream 2.0 is a fully managed non-persistent application and desktop streaming service that provides users instant access to their desktop applications from anywhere.**
- Desktop Application Streaming Service.
- Deliver to any computer, without acquiring, provisioning infrastructure.
- The application is delivered from within a web browser.

#### 18.2.1. Amazon AppStream 2.0 vs WorkSpaces

- **Workspaces:**
  - Fully managed VDI and desktop available.
  - The users connect to the VDI and open native or WAM applications.
  - Workspaces are on-demand or always on.
- **AppStream 2.0:**
  - Stream a desktop application to web browsers (no need to connect to a VDI).
  - Works with any device (that has a web browser).
  - Allow to configure an instance type per application type (CPU, RAM, GPU).

### 18.3. Amazon Sumerian

- **Amazon Sumerian is a managed service that lets you create and run 3D, Augmented Reality (AR) and Virtual Reality (VR) applications. You can build immersive and interactive scenes that run on AR and VR, mobile devices, and your web browser.**
- Create and run virtual reality (VR), augmented reality (AR), and 3D applications.
- Can be used to quickly create 3D models with animations.
- Ready-to-use templates and assets - no programming or 3D expertise required.
- Accessible via a web-browser URLs or on popular hardware for AR/VR.

### 18.4. AWS IoT Core

- **AWS IoT Core, is serverless and lets you connect billions of devices to the AWS Cloud, lets you securely connect IoT devices to the AWS Cloud and other devices without the need to provision or manage servers.**
- IoT stands for "Internet of Things" - the network of internet-connected devices that are able to collect and transfer data.
- AWS IoT Core allows you to easily connect IoT devices to the AWS Cloud.
- Serverless, secure & scalable to billions of devices and trillions of messages.
- Your applications can communicate with your devices even when they aren't connected.
- Integrates with a lot of AWS services (Lambda, S3, SageMaker, etc.).
- Build IoT applications that gather, process, analyze, and act on data.

### 18.5. Amazon Elastic Transcoder

- **Amazon Elastic Transcoder is media transcoding in the cloud. It is used to convert media files from their source format into versions that will play back on devices like smartphones, tablets, and PCs.**
- Elastic Transcoder is used to convert media files stored in S3 into media files in the formats required by consumer playback devices (phones etc..)
- Benefits:
  - Easy to use.
  - Highly scalable - can handle large volumes of media files and large file sizes.
  - Cost effective - duration-based pricing model.
  - Fully managed & secure, pay for what you use.

### 18.6. AWS Device Farm

- **AWS Device Farm is an application testing service that lets you improve the quality of your web and mobile apps by testing them across an extensive range of desktop browsers and real mobile devices; without having to provision and manage any testing infrastructure.**
- Fully-managed service that tests your web and mobile apps against desktop browsers, real mobile devices, and tablets.
- Run tests concurrently on multiple devices (speed up execution).
- Ability to configure device settings (GPS, language, Wi-Fi, Bluetooth, ...).

### 18.7. AWS Backup

- **AWS Backup is a centralized backup service that makes it easy and cost-effective for you to backup your application data across AWS services in the AWS Cloud. CloudEndure Disaster Recovery minimizes downtime and data loss by providing fast, reliable recovery into AWS of your physical, virtual, and cloud-based servers.**
- Fully-managed service to centrally manage and automate backups across AWS services.
- On-demand and scheduled backups.
- Supports PITR (Point-in-time Recovery).
- Retention Periods, Lifecycle Management, Backup Policies, ...
- Cross-Region Backup.
- Cross-Account Backup (using AWS Organizations).

#### 18.7.1. Disaster Recovery Strategies

- Backup and Restore (Cheapest)
- Pilot Light
- Multi-Site / Hot-Site
- Warm Standby

### 18.8. AWS Elastic Disaster Recovery (DRS)

- Used to be named "CloudEndure Disaster Recovery".
- Quickly and easily recover your physical, virtual, and cloud-based servers into AWS.
- Example: protect your most critical databases (including Oracle, MySQL, and SQL Server), enterprise apps (SAP), protect your data from ransomware attacks, ...
- Continuous block-level replication for your servers.

### 18.9. AWS DataSync

- Move large amount of data from on-premises to AWS.
- Can synchronize to: Amazon S3 (any storage classes - including Glacier), Amazon EFS, Amazon FSx for Windows.
- Replication tasks can be scheduled hourly, daily, weekly.
- The replication tasks are **incremental** after the first full load.

### 18.10. AWS Fault Injection Simulator (FIS)

- A fully managed service for running fault injection experiments on AWS workloads.
- Based on **Chaos Engineering** - stressing an application by creating disruptive events (e.g., sudden increase in CPU or memory), observing how the system responds, and implementing improvements.
- Helps you uncover hidden bugs and performance bottlenecks.
- Supports the following AWS services: EC2, ECS, EKS, RDS...
- Use pre-built templates that generate the desired disruptions.

## 19. AWS related Abbreviations & Acronyms

### 19.1. A

- AWS Amazon Web Services
- Amazon ES Amazon Elasticsearch Service
- AMI Amazon Machine Image
- API Application Programming Interface
- AI Artificial Intelligence
- ACL Access Control List
- ALB Application Load Balancer
- ARN Amazon Resource Name
- AZ Availability Zone
- ACM AWS Certificate Management
- ASG Auto Scaling Group
- AES Advanced Encryption System
- ADFS Active Directory Federation Service
- AVX Advanced Vector Extensions

### 19.2. B

- BYOL Bring Your Own License

### 19.3. C

- CDN Content Delivery Network
- CRC Cyclic Redundancy Check
- CLI Command Line Interface
- CIDR Classless Inter-Domain Routing
- CORS Cross Origin Resource Sharing
- CRR Cross Region Replication
- CI/CD Continuous Integration/Continuous Deployment

### 19.4. D

- DMS Database Migration Service
- DNS Domain Name System
- DDoS Distributed Denial of Service
- DoS Denial of Service
- DaaS Desktop as-a-Service

### 19.5. E

- EC2 Elastic Compute Cloud
- ECS EC2 Container Service
- ECR Elastic Container Registry
- EFS Elastic File System
- EI Elastic Inference
- ENA Elastic Network Adapter
- EKS Elastic Kubernetes Service
- EBS Elastic Block Store
- EMR Elastic MapReduce
- ELB Elastic Load Balancing
- EFA Elastic Fabric Adapter
- EIP Elastic IP
- EDA Electronic Design Automation
- ENI Elastic Network Interface
- ECU EC2 Compute Unit

### 19.6. F

- FIFO First In First Out
- FaaS Function as-a-Service

### 19.7. H

- HPC High-Performance Compute
- HVM Hardware Virtual Machine
- HTTP Hypertext Transfer Protocol
- HTTPS HTTP Secure
- HDK Hardware Development Kit

### 19.8. I

- IAM Identity & Access Management
- iOT Internet Of Things
- S3 IA S3 Infrequent Access
- iSCSI Internet Small Computer Storage Interface
- IOPS Input/Output Operation Per Second
- IGW Internet Gateway
- ICMP Internet Control Message Protocol
- IP Internet Protocol
- IPSec Internet Protocol Security
- IaaS Infrastructure-as-a-Service

### 19.9. J

- JSON JavaScript Object Notation

### 19.10. K

- KMS Key Management Service
- KVM Kernel-based Virtual Machine

### 19.11. L

- LB Load Balancer
- LCU Load Balancer Capacity Unit

### 19.12. M

- MFA Multi-Factor Authentication
- MSTSC Microsoft Terminal Service Client
- MPP Massive Parallel Processing
- MITM Man in the Middle Attack
- ML Machine Learning
- MPLS Multi Protocol Label Switching

### 19.13. N

- NACL Network Access Control List
- NLP Natural Language Processing
- NFS Network File System
- NS Name Server
- NAT Network Address Translation
- NVMe Non-Volatile Memory Express

### 19.14. O

- OLTP Online Transaction Processing
- OLAP Online Analytics Processing
- OCI Open Container Initiative

### 19.15. P

- PCI DSS Payment Card Industry Data Security Standard
- PVM Para Virtual Machine
- PV ParaVirtual
- PaaS Platform as a Service

### 19.16. Q

- QLDB Quantum Ledger Database

### 19.17. R

- RAIDRedundant Array of Independent Disk
- RDS Relational Database Service
- RRS Reduced Redundancy Storage
- RI Reserved Instance
- RAM Random-access Memory
- RIE Runtime Interface Emulator

### 19.18. S

- SSEServer Side Encryption
- S3 Simple Storage Service
- S3 RTC S3 Replication Time Control
- SRR Same Region Replication
- SMS Server Migration Service
- SWF Simple Workflow Service
- SES Simple Email Service
- SNS Simple Notification Service
- SQS Simple Queue Service
- SES Simple Email Service
- SLA Service Level Agreement
- SSL Secure Socket Layer
- SOA Start of Authority
- SDK Software Development Kit
- SSH Secure Shell
- SAR Serverless Application Repository
- SRD Scalable Reliable Datagrams
- SSO Single Sign-On
- SAML Security Assertion Markup Language
- SaaS Software-as-a-Service
- SaaS Security-as-a-Service
- SCP Service Control Policies
- SCA Storage Class Analysis
- STS Security Token Service
- SNI Server Name Indication

### 19.19. T

- TTL Time To Live
- TLS Transport Layer Security
- TPM Trusted Platform Module
- TME Total Memory Encryption
- TPM Technical Program Manager
- TPS Transaction Per Second
- TCP Transmission Control Protocol

### 19.20. V

- VPC Virtual Private Cloud
- VM Virtual Machine
- VTL Virtual Tape Library
- VPN Virtual Private Network
- VLAN Virtual Local Area Network
- VDI Virtual Desktop Infrastructure
- VPG Virtual Private Gateway

### 19.21. W

- WAFWeb Application Firewall

## 20. Commands

- List of AWS Regions
  - aws ec2 describe-regions
- Find AWS availability zones using AWS CLI
  - aws ec2 describe-availability-zones --region `region`
