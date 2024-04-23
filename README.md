Static Web App Deployment on AWS with Docker, Amazon ECR, and Amazon ECS
This project involves deploying a static web application on AWS using Docker containers, Amazon Elastic Container Registry (ECR), and Amazon Elastic Container Service (ECS). Below is a detailed guide on how to deploy the web app along with the necessary prerequisites and steps involved.

Prerequisites
Install Git and Visual Studio:
Install Git and Visual Studio on your computer.
Register for a GitHub account and create a Key Pair. Add the Public SSH Key to GitHub.
Docker Setup:
Signup for a Docker Hub Account.
Download and Install Docker on your computer.
AWS Setup:
Install AWS CLI.
Create an IAM User and Named Profile.
Deployment Steps
1. Docker Configuration
Create a Dockerfile for your static web application.
Build the Docker container.
Create a repository in your Docker Hub account.
Push the Docker image to your Docker Hub repository.
2. Amazon ECR Setup
Create an Amazon ECR repository to store your Docker image.
Push the Docker image to your ECR repository.
3. AWS Infrastructure Setup
Create a VPC with public and private subnets in 2 availability zones.
Create resources such as NAT Gateway, Bastion Host, and Application Load Balancer using Public Subnets.
Configure Security Groups to control inbound and outbound traffic.
Create an Application Load Balancer to distribute web traffic to the containers.
4. Amazon ECS Configuration
Create an ECS Cluster to run your containers.
Create a Task Definition specifying the Docker image, CPU, memory, and container ports.
Create a Service to maintain a specified number of running instances of a task definition within an ECS cluster.
5. Domain Setup
Use Route 53 to register your domain name and create a record set pointing to the Application Load Balancer.
Use AWS Certificate Manager to secure communications from the end user to the web server.
Conclusion
By following these steps, you can deploy your static web application on AWS with Docker containers, Amazon ECR, and Amazon ECS. This setup provides scalability, reliability, and security for hosting your application on the cloud. Additionally, integrating Route 53 and AWS Certificate Manager ensures proper domain setup and secure communications for your web application.






