# AWS EC2 Instance Notes

This repository contains detailed notes and explanations about various AWS EC2 services and related concepts. The notes cover topics like EC2 instance types, AMI & tenancy, VPC, subnetting, instance states, instance access, storage, networking, recovery options, purchasing models, and more. The goal of these notes is to help understand and navigate EC2 services and make informed decisions when working with AWS EC2 instances.

## Table of Contents

1. EC2 Instance Types
2. AMI & Tenancy
3. Regions & Availability Zones (AZs)
4. VPC & Subnets
5. Instance States
6. Accessing EC2 Instances
7. Amazon Machine Images (AMIs)
8. EC2 Storage Options
9. EC2 Networking
10. Recovery from Failures
11. EC2 Purchasing Options
12. Security Groups
13. Auto Scaling
14. Elastic Load Balancing (ELB)
15. Designing for Resilience & Availability
16. Step-by-Step EC2 Launching
17. Project


## EC2 Instance Types

EC2 offers a variety of instance types optimized for different use cases such as compute-intensive, memory-intensive, and storage-optimized workloads. Learn about the different families like T, M, C, R, I, and P instance types and their ideal use cases.

## AMI & Tenancy

- **AMI (Amazon Machine Image)**: An AMI is a pre-configured template for your instances. You can either use default AMIs or create custom AMIs with your desired configurations.
- **Tenancy**: EC2 instances can be launched with either shared or dedicated tenancy. Dedicated tenancy means the instance runs on hardware dedicated to a single customer.

## Regions & Availability Zones (AZs)

AWS resources are spread across different geographical regions. Each region contains multiple Availability Zones (AZs). Deploying instances across multiple AZs improves fault tolerance and increases application availability.

## VPC & Subnets

A **VPC (Virtual Private Cloud)** allows you to define a virtual network within AWS. VPCs are segmented into **subnets**, which can be public or private. Subnets provide the ability to separate and control access to your instances.

## Instance States

EC2 instances can be in various states such as:

- **Pending**: Instance is being created.
- **Running**: Instance is up and running.
- **Stopping**: Instance is shutting down.
- **Stopped**: Instance is not running, but the data persists.
- **Terminated**: Instance is deleted.

## Accessing EC2 Instances

You can access EC2 instances through different methods:

- **SSH (for Linux)**: Use SSH to access Linux-based instances.
- **RDP (for Windows)**: Use Remote Desktop Protocol (RDP) for Windows-based instances.

## Amazon Machine Images (AMIs)

AMIs are the templates used to launch instances. They include the OS, application server, and applications. Custom AMIs allow for faster instance deployment with pre-configured software.

## EC2 Storage Options

EC2 provides various storage options, including:

- **EBS (Elastic Block Store)**: Persistent block storage attached to EC2 instances.
- **Instance Store**: Temporary storage that is tied to the lifecycle of an instance.
- **EFS (Elastic File System)**: Managed file storage for use with EC2 instances.
- **S3 (Simple Storage Service)**: Object storage that can be used for storing large amounts of data.

## EC2 Networking

Networking features like **Elastic IP** addresses, **Security Groups**, **VPC Peering**, and **VPN Connections** are essential to control how EC2 instances communicate with each other and external resources.

## Recovery from Failures

AWS provides multiple options for recovering from instance or service failures:

- **EC2 Auto Recovery**: Automatically recover instances when a failure is detected.
- **Snapshots & Backups**: Take EBS snapshots or use AWS Backup to restore instances.
- **Elastic Load Balancing (ELB)** and **Auto Scaling** ensure high availability during failures by automatically adjusting capacity.

## EC2 Purchasing Options

AWS offers several purchasing models to optimize costs:

- **On-Demand Instances**: Pay for compute capacity by the second.
- **Reserved Instances**: Commit to a specific instance type for 1-3 years to receive a discount.
- **Savings Plans**: Flexibly commit to usage in exchange for a discount over time.
- **Spot Instances**: Bid on unused EC2 capacity at up to 90% off on-demand prices.
- **Dedicated Hosts/Instances**: Lease dedicated physical servers or place instances on isolated hardware.

## Security Groups

Security Groups act as a virtual firewall to control inbound and outbound traffic to EC2 instances. They are stateful and can be configured for specific protocols, IP addresses, and ports.

## Auto Scaling

**Auto Scaling** ensures that the number of EC2 instances adjusts automatically according to demand. You can set minimum, maximum, and desired instance counts, as well as scaling policies to manage load effectively.

## Elastic Load Balancing (ELB)

ELB automatically distributes incoming traffic across multiple instances in one or more Availability Zones. There are three types of load balancers:

- **Application Load Balancer (ALB)**: Ideal for HTTP/HTTPS traffic.
- **Network Load Balancer (NLB)**: Suitable for TCP, UDP, and low-latency applications.
- **Gateway Load Balancer (GLB)**: For deploying third-party virtual appliances.

## Designing for Resilience & Availability

Designing for availability involves using strategies like **multi-AZ deployments**, **Auto Scaling**, and **Elastic Load Balancing**. AWS services such as EC2 and S3 can be combined to create fault-tolerant, highly available architectures.

## Step-by-Step EC2 Launching

Learn how to launch an EC2 instance by following these steps:

1. Select an AMI.
2. Choose an instance type.
3. Configure instance details, including VPC and subnet.
4. Add storage (EBS or Instance Store).
5. Configure security groups for network access.
6. Launch the instance and connect via SSH or RDP.

## Project

This section provides a sample project that walks through the process of setting up a basic EC2 infrastructure with load balancing, auto-scaling, and a multi-tier architecture.

## Usage

Clone this repository to access all the notes and tutorials related to AWS EC2 services and architecture.

```bash
git clone https://github.com/Ayush-Rathor/EC2-Beginner-to-Pro.git
