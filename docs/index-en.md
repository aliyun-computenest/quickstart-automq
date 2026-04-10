# AutoMQ for Kafka BYOC Edition User Guide

## Overview

AutoMQ for Kafka BYOC (Bring Your Own Cloud) Edition is a next-generation commercial distribution of Kafka, redesigned and implemented by AutoMQ based on cloud-native infrastructure. It supports private installation and self-management within public cloud VPC (Virtual Private Cloud) environments.

While maintaining 100% compatibility with Apache Kafka, AutoMQ provides users with over 50% cost savings and 100x elasticity advantages. It also supports second-level partition migration and automatic traffic rebalancing, addressing common operational pain points.

The AutoMQ for Kafka BYOC Edition utilizes Alibaba Cloud Compute Nest for private deployment, deploying the AutoMQ Kafka software into user-defined VPCs and subnets. Subsequent access to the service remains entirely within the user's private network.

AutoMQ for Kafka also offers a fully managed SaaS version. For more details, please refer to the [AutoMQ Official Website](https://automq.com/).

## Billing Information

Since the AutoMQ for Kafka BYOC Edition deploys software on resource instances under the user's account, users are required to pay for the following resources:

**Cloud Resource Costs (Paid directly to Alibaba Cloud)**

The underlying paid cloud resources mainly include:
- **ECS Instances**: AutoMQ Kafka requires ECS instances to deploy the control plane and Kafka cluster data nodes.
- **EBS Disks**: AutoMQ Kafka requires a small amount of cloud disk storage for server logs and basic metadata.
- **OSS Storage**: AutoMQ Kafka uses OSS (Object Storage Service) to store message data, which incurs costs for OSS storage space and API calls.
- **Public Network Fees (Optional)**: If users choose to access the console and services via the public internet, public network traffic fees may apply.

**Software Service Fees (Paid to AutoMQ)**

AutoMQ Kafka provides commercial BYOC services to enterprise customers. Therefore, software service fees are charged based on the usage volume of the user's cluster. For detailed billing information, please refer to the [documentation](https://docs.automq.com/zh/automq-cloud/subscriptions-and-billings/byoc-env-billings/billing-instructions-for-byoc).

The current billing methods for the BYOC Edition include:
- Pay-As-You-Go (billed hourly) and Subscription (billed by License specification).
- Billing Metric: Based on the cluster's AKU (AutoMQ Kafka Unit) processing specification.

**Important**: AutoMQ Kafka BYOC Edition only charges for actually created clusters. No fees are incurred when simply activating the Kafka service; billing based on the cluster's AKU specification begins only when an instance (cluster) is created in the AutoMQ Kafka console.

Currently, AutoMQ Kafka BYOC Edition supports deployment on the following ECS instance specifications:

| Instance Family | vCPU & Memory | System Disk | Public Bandwidth |
|---------------|-------------------| --- | --- |
| ecs.r7.large | Memory-optimized r7, 2 vCPU, 16 GiB | ESSD Cloud Disk 40 GiB PL0 | Customizable as needed |
| ecs.r6.large | Memory-optimized r6, 2 vCPU, 16 GiB | ESSD Cloud Disk 40 GiB PL0 | Customizable as needed |
| ecs.u1-c1m8.large | General Purpose u1, 2 vCPU, 16 GiB | ESSD Cloud Disk 40 GiB PL0 | Customizable as needed |

For additional specifications or other services (such as high availability requirements for clusters, enterprise-level support services, etc.), please [contact us](https://automq.com/).

## Deployment Architecture

## Prerequisite 1: Cloud Account Permissions

To activate and use the AutoMQ Kafka BYOC Edition service, the operating cloud account must have the following permissions:
1. Create authorization policies and roles.
2. Activate products from the Cloud Marketplace.

It is generally recommended to use the primary account or a subordinate account with administrative privileges for these operations.

## Prerequisite 2: Required Cloud Services Activated

The AutoMQ Kafka BYOC Edition depends on the following cloud products. It is recommended to activate them in advance:
1. [Elastic Compute Service (ECS)](https://ecs.console.aliyun.com).
2. [Object Storage Service (OSS)](https://oss.console.aliyun.com).
3. [PrivateZone](https://dnsnext.console.aliyun.com).

## Usage Process

Once the prerequisites above are met, subscribe to the AutoMQ Kafka BYOC Edition service.

After activation, please visit the [AutoMQ BYOC Edition Documentation Center](https://docs.automq.com/zh/automq-cloud/getting-started/install-byoc-environment/alibaba-cloud) for detailed usage processes and operational instructions.

## Contact Us

Welcome to contact us through the following channels for more information.

💻 Official Website: https://www.automq.com

💻 Documentation Center: https://www.automq.com/docs

🌟 GitHub: https://github.com/AutoMQ/automq

👀 Bilibili: AutoMQ Official Account

🔍 WeChat QR Code:

![QR Code](qrcode.png)
