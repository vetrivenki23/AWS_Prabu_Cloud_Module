# Terraform AWS EC2 Instance

This Terraform code deploys an Amazon Elastic Compute Cloud (EC2) instance in AWS. You can use this code as a starting point to launch EC2 instances with specific configurations.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- [Terraform](https://www.terraform.io/downloads.html) installed on your local machine.
- AWS credentials properly configured. You can use the [AWS CLI](https://aws.amazon.com/cli/) to set up your credentials.

## Usage

1. Clone this repository or copy the `tf_ec2` resource block into your Terraform configuration file.

2. Customize the `ami` and `instance_type` variables in the resource block according to your requirements. You can also modify other resource attributes as needed.

```hcl
resource "aws_instance" "tf_ec2" {
  ami           = var.ec2_ami
  instance_type = var.ec2_type
  user_data     = file("userdata.sh")

  tags = {
    Name = "Prabu-EC2Cloud"
  }
}
