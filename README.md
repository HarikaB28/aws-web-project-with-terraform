# Terraform AWS Webserver Project

## Project Description
This is a complete, working Infrastructure-as-Code (IaC) project built using **Terraform** to deploy a functional, reliable, and secure web hosting environment on **Amazon Web Services (AWS)**. 

Based on the architecture diagram, this project automatically provisions a custom Virtual Private Cloud (VPC) that hosts two separate public subnets. An Application Load Balancer (ALB) sits at the front door of the network to receive incoming user traffic and split the workload evenly across two EC2 instances running Apache web servers. Additionally, the setup includes private, direct network connectivity to an Amazon S3 bucket via a VPC Gateway Endpoint, ensuring data storage traffic never has to travel over the public internet.

## Key Features & Infrastructure Components
* **Custom AWS VPC Network:** A fully configured virtual network isolated securely within your AWS account.
* **Application Load Balancing:** A front-end load balancer that dynamically manages traffic distribution and automatically redirects users away from a server if it goes down.
* **Dual Public Subnets:** Built across two availability zones to ensure the project remains up and running even if one AWS data center experiences an issue.
* **Automated Web Servers:** Two EC2 instances that automatically install Apache and launch a "welcome to webserver" homepage upon their very first boot using a separate User Data bash script.
* **Secure S3 Storage Integration:** Direct network paths to Amazon S3 using integrated IAM roles, avoiding the need to hardcode dangerous AWS security keys inside the server code.

