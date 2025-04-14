# Build-Secure-Multitier-WebApp-AWS
Build A Secure, Scalable and Resilient Web Application

## Introduction:
The primary goal of this project was to build a multi-tier architecture while following strong security principles across all layers—from the CDN and web tier to the database layer. I implemented strict security controls, encryption mechanisms, and continuous monitoring to prevent unauthorized access and ensure compliance with best practices. This Project demonstrates the hosting a blog website in VPC from scratch and hosting a website Scalable, Reliable, Secure and cost optimized on AWS using various AWS Services. The Static website consists of html, css and js is deployed in S3 static website for High durability and availability and its fronted with the cloudfront for providing the low latency, high performance frontend to the endusers. The backend is running in EC2 deployed across multiple AZs for high availability and its tied with the RDS MYSQL[Primary-Backup setup] for the data layer which is also deployed across multi-AZ.


## Project Highlights:

1. VPC
   * Created the VPC from scratch with public, private, and database subnets across multiple Availability Zones.

2. ALB:
   * Leveraged Application Load balancer for the high availability and for the efficient traffic distribution across multiple Azs

3. EC2:
   * Used as Compute for the static and dynamic application and present across multiple AZs for High availability.

4. RDS:
   * RDS Mysql is used as database for the application with primary and standby for Multi-Az deployment.

5. S3:
   * Stored the static web pages in the S3 for high durability.

6. KMS:
   * Created the customer managed KMS key for efficient security and used to encrypt the block storage volume.

7. Inspector:
   * Configured AWS Inspector  to EC2 instances for efficiently identifying the vulnerability across Multi-Azs

8. Config:
   * To identity Complaince status for the CDN and S3, leveraged AWS Config.
  
9. ASG:
    * Created the ASG for the EC2 instances for automatic scaling of instances if the instances goes down or high demand of traffic.

10. Launch Template:
    * Leveraged Launch template by configuring the OS, installing the web server and copying the Static files from S3 to reduce the application installing time once the instances are launched.

11. ACM:
    * Created the public certificate in certificate manager for seamless certificate management and used in CDN
   
12. Route 53:
    * Created the domain in public hosted zone and leveraged Route 53 for the resolving the Ip address from the internet.

