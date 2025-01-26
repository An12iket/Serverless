# All about backend, frontend deployments using AWS (EC2, S3, Cloudfront) and serverless Architectue such as (CloudFare)...

### This repository contains my learning journey for creating and managing EC2 instances, S3 buckets, cloudFront on AWS, nginx reverse proxies, cloudfare using Hono
## EC2 Learning 
## Objectives
- Understand the basics of AWS EC2.
- Learn to create and configure EC2 instances.
- Explore security groups, key pairs, and instance management.
## Topics Covered
1. **Creating an EC2 Instance**  
   - Choosing the instance type.  
   - Configuring storage and security.  
   - Launching and connecting to the instance.

2. **Security Groups**  
   - Setting up inbound and outbound rules.  
   - Managing access to the instance.

3. **Key Pairs**  
   - Generating and using key pairs for SSH access.  
   - Managing key pair files securely.

4. **Instance Management**  
   - Starting, stopping, and terminating instances.  
   - Monitoring instance performance.

---

# Learning Nginx Reverse Proxies

## What I Learned

- **Reverse Proxy Basics**:  
  A reverse proxy acts as an intermediary between clients and backend servers, forwarding client requests and returning server responses.

- **Why Use Nginx**:  
  - Lightweight and fast.
  - Handles high concurrency efficiently.
  - Supports load balancing, caching, and SSL termination.

- **Key Concepts**:  
  - Configuring `server` blocks for routing traffic.
  - Forwarding requests to multiple backend servers.
  - Securing connections with SSL.

## Example Nginx Reverse Proxy Configuration

```nginx
server {
    listen 80;
    server_name example.com;

    location / {
        proxy_pass http://localhost:3000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}

```
--- 
# Frontend Deployment with AWS S3 and CloudFront

Today, I learned how to deploy a frontend application using **AWS S3** and **CloudFront**. Here's a quick overview of the process:
## Steps to Deploy

### 1. Set Up S3 Bucket
- Create an S3 bucket.
- Enable static website hosting.
- Upload the frontend build files (HTML, CSS, JS, etc.).
- Set proper bucket policies to make the content publicly accessible.

### 2. Configure CloudFront
- Create a CloudFront distribution.
- Set the S3 bucket as the origin.
- Configure caching and distribution settings.
- Use the CloudFront domain name for accessing the deployed application.

This approach ensures a scalable, secure, and globally distributed frontend deployment.
---

## Tools Used
- **AWS Management Console**
- **AWS CLI**

---

## Resources
- [AWS Documentation](https://docs.aws.amazon.com/)
- [AWS Free Tier](https://aws.amazon.com/free/)
- [AWS S3](https://aws.amazon.com/pm/serv-s3/?gclid=Cj0KCQiA19e8BhCVARIsALpFMgFb0UJnsCKUzO8Pm9y9928a20HpDlXXWhlnk8OTqMmRveM3hz9XlbcaAjx-EALw_wcB&trk=b8b87cd7-09b8-4229-a529-91943319b8f5&sc_channel=ps&ef_id=Cj0KCQiA19e8BhCVARIsALpFMgFb0UJnsCKUzO8Pm9y9928a20HpDlXXWhlnk8OTqMmRveM3hz9XlbcaAjx-EALw_wcB:G:s&s_kwcid=AL!4422!3!536397139414!p!!g!!amazon%20s3%20cloud%20storage!11539706604!115473954194)
- [AWS EC2](https://aws.amazon.com/pm/ec2/?gclid=Cj0KCQiA19e8BhCVARIsALpFMgEwpb39nGTFCdoF_XJsGrR2L_ed8U8Rv1JmnVeRxZOXHmPlYjtgArYaAhVyEALw_wcB&trk=32f4fbd0-ffda-4695-a60c-8857fab7d0dd&sc_channel=ps&ef_id=Cj0KCQiA19e8BhCVARIsALpFMgEwpb39nGTFCdoF_XJsGrR2L_ed8U8Rv1JmnVeRxZOXHmPlYjtgArYaAhVyEALw_wcB:G:s&s_kwcid=AL!4422!3!476942909971!e!!g!!aws%20ec2!11539707735!118057053088)
- [nginx doc](https://nginx.org/en/docs/)
- [Hono doc](https://hono.dev/docs/)
