# Terraform AWS Glue ETL Pipeline

## Overview

This project demonstrates how to provision a complete AWS Glue ETL pipeline using Terraform. The infrastructure creates S3 buckets for source data, processed data, and ETL scripts, along with the required IAM roles and Glue resources to crawl and process the dataset.

The goal of this project is to show how Infrastructure as Code (IaC) can automate data engineering workflows on AWS.

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
