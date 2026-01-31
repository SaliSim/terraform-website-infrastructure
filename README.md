# terraform-website-infrastructure

## This is a simple static website hosted in a gcs bucket.
This project deploys a HTML based website in cloud storage.
All the reources are provisioned by terraform

## Prerequisites
- GCP account with billing account.
- Enable the APIs as below:
  - gcloud services enable \
  - compute.googleapis.com \
  - storage.googleapis.com \
  - dns.googleapis.com \
  - cloudresourcemanager.googleapis.com
- DNS zone setup
- Terraform installed 

## Quick deploy
```bash
git clone https://github.com/SaliSim/terraform-website-infrastructure.git
terraform init
terraform plan
terraform apply
terraform destroy #when the resources are no longer required
```
## What get's created
---
- _Google cloud storage bucket_
- _Cloud DNS Zone_
- _Global HTTPS Load balancer_
- _Static IP address_
- _Cloud CDN configuration_
- _DNS record_
- _SSL certificate_
---
 
## Configurations
## Required Variables
```hcl
project_id = "your-project-id"
region     = "us-central1"
```



