#Project Scenario:

A small to medium-sized digital marketing agency, "DigitalBoost" wants to enhance its online presence by creating a high-performance WordPress-based website for their clients. The agency needs a scalable, secure, and cost-effective solution that can handle increasing traffic and seamlessly integrate with their existing infrastructure. Your task as an AWS Solutions Architect is to design and implement a WordPress solution using various AWS services, such as Networking, Compute, Object Storage, and Databases.

#Wordpress Captone Project Documentation:

#VPC Setup:

1. I defined the correct ip ranges and created a VPC
2. I created an Internet Gateway and attached it to my VPC
3. I created three subnets, two public subnets and 1 private subnet
4. I created a route table that's configured to the public and private subnet

#WORDPRESS INSTANCE CREATION:

1. I created my wordpress ec2 instances and configured it using the script provided.

#AWS MYSQL RDS SETUP:

1. I created my rds database for mysql
2. Configured the default security attached to the rds database to include an mysql inbound traffic, which is port 3306
3. I connected my rds database to my wordpress server

#EFS SETUP:

1. I created an efs storage (elastic file system) and mounted it on my existing wordpress instance
2. I configured my wordpress server to use the shared file system

#APPLICATION LOAD BALANCER and AUTO SCALING GROUP SETUP:

1. I created a load balancer to distribute incoming traffic among multiple instances ensuring high availability and fault tolerance.
2. I created a launch template required to create an Auto Scaling Group
3. In my launch template, I utilized the user data provided to set up my instances on first launch.
4. I integrated the application load balancer with an autoscaling group I created to implement automatic scaling of the instances based on traffic load.
