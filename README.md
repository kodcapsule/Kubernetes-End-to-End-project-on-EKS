# Kubernetes End-to-End project on EKS: AWS EKS Cluster Setup, Application Deployment, and Ingress Configuration


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