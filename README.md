# Kubernetes End-to-End project on EKS: AWS EKS Cluster Setup, Application Deployment, and Ingress Configuration

## Introduction 
Kubernetes is an open-source container orchestration platform that enables you to automate the  deployment,sacaling and  management containerised applications at scale. Kubernetes offers a lot of benefits including:
1. Auto-healing
2. Auto-scaling
3. Enterprise-support
More on Kubernetes [here](https://kubernetes.io/)

With all these benefits comes the complexity of managing Kubernetes clusters. This is where Amazon Elastic Kubernetes Service (EKS) comes into the picture. EKS provides a fully managed Kubernetes service that eliminates the complexity of operating Kubernetes clusters. EKS allows you to:
1. Deploy applications faster with less operational overhead
2. Scale seamlessly to meet changing workload demands
3. Improve security through AWS integration and automated updates
4. Choose between standard EKS or fully automated EKS Auto Mode
For further reading, you can access the [EKS official documentation](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html)

In this project, we will be creating an EKS cluster in AWS and deploying an application to that cluster. So grab a cup of coffee and let’s get started. 

## Prerequisites
**1. AWS Account:** You should have an AWS account with an IAM user with these minimal access levels. 
| AWS Service | Access Level | Details |
|-------------|--------------|---------|
| CloudFormation | Full Access | - |
| EC2 | **Full:** Tagging<br>**Limited:** List, Read, Write | Full access for tagging operations, limited access for list, read, and write operations |
| EC2 Auto Scaling | **Limited:** List, Write | Limited access for list and write operations |
| EKS | Full Access | - |
| IAM | **Limited:** List, Read, Write, Permissions Management | Limited access for list, read, write, and permissions management operations |
| Systems Manager | **Limited:** List, Read | Limited access for list and read operations |

**2. AWS CLI** installed and configure AWS CLI
   - Download from [Installing or updating to the latest version of the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

**3.kubectl** installed kubectl for cluster management from the official Kubernetes page
   - Download from [Install Tools](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

**4.eksctl** installed  eksctl CLI  used to work with EKS clusters.
   - Download from [Installation](https://eksctl.io/installation/)

**5 Knowledge and Understanding of AWS and Kubernetes** You should have some basic knowledge and skills of working with AWS, espercially AWS CLL and Kubernetes.
   

## Project Architecture


## Project Setup

### Create EKS Cluster

Creating EKS cluster
```bash
  eksctl create cluster --name <CLUSTER_NAME> --region <AWS_REGION> --fargate
```
**CLUSTER_NAME:** Name of your cluster eg. my_demo_eks_cluster
**AWS_REGION:** The region to deploy your cluster eg. us-east-1

Deleting EKS cluster
```bash
  eksctl delete cluster --name demo-cluster --region us-east-1
```