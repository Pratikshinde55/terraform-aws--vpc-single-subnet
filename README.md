## AWS VPC with Single Subnet and EC2 Deployment using Terraform

 
## Key Points:

**Single VPC Creation:**

The project sets up a Virtual Private Cloud (VPC) with a custom CIDR block (10.0.0.0/16), providing a private network range for your EC2 instances.

**Single Subnet Deployment:** 

A single subnet within a specific Availability Zone (ap-south-1a) is defined with a CIDR block (10.0.1.0/24).

**Public IP Association:**

The EC2 instance is configured to automatically receive a public IP upon launch (map_public_ip_on_launch = true), making it accessible from the internet.

**Security Group Configuration:**

A custom security group is created that allows incoming traffic on common ports such as 22 (SSH), 80 (HTTP), 443 (HTTPS), and 8080. This enables secure access to the EC2 instance for 
management and web hosting.

**Internet Gateway Setup:**

An Internet Gateway is attached to the VPC, ensuring that instances within the VPC can communicate with the internet.

**Route Table Configuration:**

A route table is created and associated with the subnet, allowing outbound internet traffic via the Internet Gateway.

**Free Tier Use:*** 

The architecture is designed to fit within the AWS Free Tier limits.

## Benefits: 

This configuration allows the deployment of a simple infrastructure with a single EC2 instance in a single subnet, perfect for small test environments, development, or educational 
use.

