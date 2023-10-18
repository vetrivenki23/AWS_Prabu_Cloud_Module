# Terraform Module: AWS EC2 Instance

This Terraform module allows you to create an Amazon Elastic Compute Cloud (EC2) instance with specific configurations.

## Usage

You can use this module by including it in your Terraform configuration file as follows:

```hcl
module "techlearnings_aws_ec2" {
  source = "app.terraform.io/your-organization/aws-ec2-instance/aws"
  version = "1.0.0"

  ami           = var.ec2_ami           # Replace with your desired AMI ID
  instance_type = var.ec2_type          # Replace with your desired instance type
  user_data     = file("userdata.sh")   # Provide a path to your user data script

  tags = {
    Name = "TechLearnings-EC2"  # Customize the tag values as needed
  }
}   
