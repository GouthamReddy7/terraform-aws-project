**Terraform Infrastructure Deployment for Web Application**    


**Overview**

This project demonstrates how to deploy a simple web application infrastructure on AWS using Terraform. The infrastructure includes:

1::VPC (Virtual Private Cloud): Creates a virtual network environment in AWS.


2::Subnets: Defines two subnets across different availability zones for high availability.


3::Internet Gateway: Enables internet access for resources within the VPC.


4::Route Tables: Routes traffic between subnets and the internet gateway.


5::Security Group: Sets up firewall rules to control traffic to EC2 instances.


6::EC2 Instances: Launches two web servers in different subnets for redundancy.


7::Application Load Balancer (ALB): Distributes incoming web traffic across the web servers.


8::Target Groups: Defines how the ALB routes traffic to the EC2 instances.

**Prerequisites**

Before you begin, ensure you have:

AWS Account: You'll need an AWS account with appropriate permissions to create resources.


Terraform Installed: Make sure you have Terraform installed on your local machine.

**Getting Started**

Clone this repository to your local machine.

git clone <repository-url>

cd <repository-directory>


**Set up your AWS credentials.**

export AWS_ACCESS_KEY_ID="your-access-key"


export AWS_SECRET_ACCESS_KEY="your-secret-key"


export AWS_DEFAULT_REGION="us-east-1" # Update with your desired region

**Initialize Terraform and apply the configuration.**

-terraform init

-terraform plan 

-terraform apply

**Access the web application.**

Once the Terraform deployment is complete, you can access your web application through the ALB DNS name provided in the output.


**Cleaning Up**{Important step to do }

To avoid unnecessary charges, destroy the resources when you're done.


-terraform destroy


Make sure to replace sensitive values like access keys and bucket names with your own.


Customize the configuration files (userdata.sh, userdata1.sh, etc.) according to your application's requirements.
