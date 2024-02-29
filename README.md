# Terraform Project Documentation

## Overview
This project aims to create a Virtual Private Cloud (VPC) along with an EC2 instance using Terraform. The objective is to set up a basic infrastructure without including a NAT Gateway to avoid incurring costs.

## Prerequisites
Before proceeding with the deployment, ensure you have the following:
- Terraform installed on your local machine
- AWS CLI configured with appropriate access keys and permissions
- Basic understanding of AWS services and networking concepts

## Getting Started
1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Run `terraform init` to initialize the Terraform configuration.
4. Run `terraform plan` to review the execution plan.
5. Run `terraform apply` to deploy the infrastructure.

## Terraform Configuration
### VPC Configuration
The VPC configuration includes:
- Creating a VPC with CIDR block `10.0.0.0/16`.
- Adding a public subnet with CIDR block `10.0.1.0/24`.
- Configuring an internet gateway and attaching it to the VPC.
- Creating a route table and associating it with the public subnet.

### EC2 Configuration
The EC2 configuration involves:
- Launching an EC2 instance within the public subnet.
- Specifying an AMI, instance type, and key pair for SSH access.
- Opening port 22 for SSH access.

## Outputs
After successfully deploying the infrastructure, you will get the following outputs:
- EC2 Instance ID
- Public IP Address of the EC2 instance

## Clean Up
To tear down the infrastructure and avoid incurring charges:
1. Run `terraform destroy`.
2. Confirm the destruction when prompted.

## Disclaimer
This project does not include a NAT Gateway, which may limit the functionality of certain AWS services that require internet access from private subnets. Consider adding a NAT Gateway for production deployments.

## Contributing
Contributions to improve this project are welcome. Feel free to submit a pull request with your enhancements.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
