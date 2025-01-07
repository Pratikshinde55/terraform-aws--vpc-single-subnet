## AWS VPC with Single Subnet and EC2 Deployment using Terraform


## Key Points:

Single VPC Creation: The project sets up a Virtual Private Cloud (VPC) with a custom CIDR block (10.0.0.0/16), providing a private network range for your EC2 instances.

Single Subnet Deployment: A single subnet within a specific Availability Zone (ap-south-1a) is defined with a CIDR block (10.0.1.0/24), ensuring the network is isolated and can be expanded later if needed.

Public IP Association: The EC2 instance is configured to automatically receive a public IP upon launch (map_public_ip_on_launch = true), making it accessible from the internet.

Security Group Configuration: A custom security group is created that allows incoming traffic on common ports such as 22 (SSH), 80 (HTTP), 443 (HTTPS), and 8080. This enables secure access to the EC2 instance for 
 management and web hosting.

Internet Gateway Setup: An Internet Gateway is attached to the VPC, ensuring that instances within the VPC can communicate with the internet.

Route Table Configuration: A route table is created and associated with the subnet, allowing outbound internet traffic via the Internet Gateway.

Terraform Automation: 
All resources, including the VPC, subnet, EC2 instance, internet gateway, and security group, are provisioned using Terraform, ensuring that the infrastructure is easily reproducible and scalable.

Free Tier Use : The architecture is designed to fit within the AWS Free Tier limits, making it cost-effective for small projects and learning purposes.

Benefits:

Simplified Infrastructure: This configuration allows the deployment of a simple infrastructure with a single EC2 instance in a single subnet, perfect for small test environments, development, or educational 
use.

Easy Management and Automation: 
With Terraform, the infrastructure can be managed as code, ensuring that changes can be tracked and rolled back if necessary. Terraform's declarative configuration also makes 
managing the infrastructure more efficient.

Scalable and Flexible: While the current setup uses a single subnet, the architecture is flexible enough to be scaled to multiple subnets or multiple Availability Zones (AZs) in the future, improving high 
availability and fault tolerance.

Security and Accessibility: The custom security group allows fine-grained control over the traffic that can reach the EC2 instance, ensuring that only authorized users can access it. The public IP configuration 
makes it simple to access the instance from anywhere.

Cost-Effective: 
The resources selected are within the AWS Free Tier, ensuring that this deployment is cost-efficient for testing, development, or educational purposes.

High Availability (Potential): With minimal adjustments, such as adding more subnets in different Availability Zones, the infrastructure can evolve into a highly available solution with failover support and load 
 balancing.
