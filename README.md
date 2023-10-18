# Terraform Module: AWS S3 Website

This Terraform module creates an S3 bucket in AWS for hosting a static website. You can use this module to provision an S3 bucket with the necessary configuration for website hosting.

## Usage

To use this module in your Terraform configuration, include the following block:

```hcl
module "website_s3_bucket" {
  source = "app.terraform.io/hcta-demo1/s3-website/aws"
  version = "1.0.1"

  bucket_name = "my-website-bucket"
  tags = {
    Name = "My Website Bucket"
  }
}
