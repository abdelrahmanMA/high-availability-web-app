# High Availability Web App Using CloudFormation

This project is the 2nd project is part of Udacity Cloud Devops nanodegree
Working URL: http://hawau-webap-1hdogtwn74coq-1624604623.us-east-1.elb.amazonaws.com/
This link will be taken down after the review
***
## Scenario
Your company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket.

You have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure.

This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.
****

## Server specs

*   You'll need to create a Launch Configuration for your application servers in order to deploy four servers, two located in each of your private subnets. The launch configuration will be used by an auto-scaling group.


*   You'll need two vCPUs and at least 4GB of RAM. The Operating System to be used is Ubuntu 18. So, choose an Instance size and Machine Image (AMI) that best fits this spec.


*   Be sure to allocate at least 10GB of disk space so that you don't run into issues.

## Security Groups and Roles

1. Since you will be downloading the application archive from an S3 Bucket, you'll, need to create an IAM Role that allows your instances to use the S3 Service.


2. Udagram communicates on the default HTTP Port: 80, so your servers will need this inbound port open since you will use it with the Load Balancer and the Load Balancer Health Check. As for outbound, the servers will need unrestricted internet access to be able to download and update their software.


3. The load balancer should allow all public traffic (0.0.0.0/0) on port 80 inbound, which is the default HTTP port. Outbound, it will only be using port 80 to reach the internal servers.


4. The application needs to be deployed into private subnets with a Load Balancer located in a public subnet.


5. One of the output exports of the CloudFormation script should be the public URL of the LoadBalancer. Bonus points if you add http:// in front of the load balancer DNS Name in the output, for convenience.

---
**NOTE:** The cloudformation scripts provied in this repo doesn't follow all of the requirements for the sake of being eligible for free-tier

---