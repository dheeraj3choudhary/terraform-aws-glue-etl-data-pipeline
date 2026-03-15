<div align="center">

# Terraform AWS Glue ETL Pipeline
This project demonstrates how to provision a complete AWS Glue ETL pipeline using Terraform. The infrastructure creates S3 buckets for source data, processed data, and ETL scripts, along with the required IAM roles and Glue resources to crawl and process the dataset. The goal of this project is to show how Infrastructure as Code (IaC) can automate data engineering workflows on AWS.


[![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/)
[![Amazon ECS](https://img.shields.io/badge/Amazon_ECS-FF9900?style=for-the-badge&logo=amazon-ecs&logoColor=white)](https://aws.amazon.com/ecs/)
[![AWS Fargate](https://img.shields.io/badge/AWS_Fargate-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/fargate/)
[![Amazon ECR](https://img.shields.io/badge/Amazon_ECR-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/ecr/)
[![AWS Glue](https://img.shields.io/badge/AWS_Glue-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/glue/)
[![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)](https://aws.amazon.com/s3/)
[![Amazon EC2](https://img.shields.io/badge/Amazon_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)](https://aws.amazon.com/ec2/)
[![Elastic Load Balancer](https://img.shields.io/badge/Elastic_Load_Balancer-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/elasticloadbalancing/)
[![IAM](https://img.shields.io/badge/AWS_IAM-DD344C?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/iam/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)

<a href="https://www.buymeacoffee.com/Dheeraj3" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" height="50">
</a>

## [Subscribe](https://www.youtube.com/@dheeraj-choudhary?sub_confirmation=1) to learn more About Artificial-Intellegence, Machine-Learning, Cloud & DevOps.

<p align="center">
<a href="https://www.linkedin.com/in/dheeraj-choudhary/" target="_blank">
  <img height="100" alt="Dheeraj Choudhary | LinkedIN"  src="https://user-images.githubusercontent.com/60597290/152035581-a7c6c0c3-65c3-4160-89c0-e90ddc1e8d4e.png"/>
</a> 

<a href="https://www.youtube.com/@dheeraj-choudhary?sub_confirmation=1">
    <img height="100" src="https://user-images.githubusercontent.com/60597290/152035929-b7f75d38-e1c2-4325-a97e-7b934b8534e2.png" />
</a>    
</p>

</div>

## Architecture

Source Data (CSV) -> S3 Source Bucket -> Glue Crawler -> Glue Data Catalog -> Glue ETL Job -> Target S3 Bucket

## Project Structure

```
.
├── buckets.tf
├── catalog_crawler.tf
├── glue_service_role.tf
├── providers.tf
├── vars.tf
├── versions.tf
├── data/
│   └── organizations.csv
└── scripts/
    └── script.py
```

## Resources Created

This Terraform configuration provisions the following AWS resources:

* Amazon S3 buckets for source data, processed output, and ETL scripts
* AWS Glue crawler for schema discovery
* AWS Glue Data Catalog table
* AWS Glue ETL job
* IAM role and policies required for Glue execution

## Prerequisites

Before running this project ensure you have:

* AWS CLI configured
* Terraform installed (>=1.x)
* AWS account with sufficient permissions

## Deployment Steps

Clone the repository

```
git clone <repo-url>
cd terraform-aws-glue-etl-pipeline
```

Initialize Terraform

```
terraform init
```

Review execution plan

```
terraform plan
```

Deploy infrastructure

```
terraform apply
```

After deployment:

1. Upload the dataset to the source S3 bucket
2. Run the Glue crawler to create the schema
3. Trigger the Glue ETL job
4. Verify processed output in the target S3 bucket

## Cleanup

To destroy all resources created by Terraform:

```
terraform destroy
```

## Learning Objectives

This project demonstrates:

* Infrastructure as Code using Terraform
* AWS Glue crawler configuration
* Glue ETL job orchestration
* IAM role setup for Glue services
* Data pipeline automation on AWS

## Use Cases

* Data lake ingestion pipelines
* Automated schema discovery
* Batch ETL pipelines
* Serverless data processing

## Author

Dheeraj Choudhary

AWS Hero | HashiCorp Ambassador | DevOps & Cloud Educator

## License

This project is for educational and demonstration purposes.
