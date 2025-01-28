**How to deploy Keycloak in an AWS ECS cluster**
Keycloak is an open-source identity and access management solution that offers authentication and authorization capabilities. It provides features such as single sign-on (SSO), user federation, identity brokering and social login.

Amazon Elastic Container Service (ECS) is a fully managed container orchestration service provided by AWS. It allows you to run and manage Docker containers on a cluster of Amazon EC2 instances or using AWS Fargate, which is a serverless compute engine for containers.

This project contains a Docker file to build a Docker image for Keycloak and two AWS CloudFormation templates to deploy Keycloak on ECS running with Fargate and RDS PostgreSQL database.

The first template prepares the infrastructure for the deployment. It creates a VPC with public and private subnets, Internet Gateway, NAT Gateways and a RDS PostgreSQL instance for Keycloak.

The second template deploys an ECS cluster with a Keycloak service running on Fargate, an Auto Scaling group for the ECS tasks, an Application Load Balancer (ALB) and Route 53 DNS configuration.

Here is the architecture diagram of the solution:
https://github.com/Silas-cloudspace/PROJECTS-AWS-CLOUDFORMATION/blob/main/deploying_keycloak_in_ecs/diagram/Keyclaok-ECS-RDS.png?raw=true 
