# AWS EC2 Auto Scaling with Load Balancer Project

## Overview

This project sets up an AWS infrastructure that includes an Auto Scaling group of EC2 instances serving a static HTML page. The instances are balanced and exposed through an Application Load Balancer (ALB). The infrastructure's provisioning and updating are automated using AWS CloudFormation with buildspec.yaml for continuous deployment

## Architecture

The project includes the following AWS resources:

- **Amazon EC2 Instances**: Autoscaled based on CPU utilization, serving a static HTML page.
- **Auto Scaling Group**: With a minimum of 2 instances and a maximum of 4, scaling is triggered when CPU utilization exceeds 90%.
- **Application Load Balancer (ALB)**: Distributes incoming traffic among EC2 instances within the Auto Scaling group.
- **AWS CloudFormation**: Manages the provisioning of the AWS resources.
- **AWS CodeBuild**: Builds the project as defined in the buildspec file.

## Project Structure
|-- aws-cfn-asg-ec2.yaml # CloudFormation template for the infrastructure
|
|-- buildspec.yml # Build specifications for AWS CodeBuild
|
|-- README.md # This file


## Prerequisites

- AWS CLI installed and configured
- IAM roles for AWS CodePipeline and AWS CodeBuild with necessary permissions
- GitHub repository for source control

## Deployment

**Clone the Repository**:

```bash
git clone <repository-url>

