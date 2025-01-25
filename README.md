My first cloud server - 
http://ec2-13-60-65-93.eu-north-1.compute.amazonaws.com:8080/todos



# Serverless Bakends using CloudFare workers and...

# EC2 Learning 

This repository contains my learning journey for creating and managing EC2 instances on AWS, nginx reverse proxies, cloudfare using Hono

---

## Objectives
- Understand the basics of AWS EC2.
- Learn to create and configure EC2 instances.
- Explore security groups, key pairs, and instance management.

---

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

## Tools Used
- **AWS Management Console**
- **AWS CLI**

---

## Resources
- [AWS Documentation](https://docs.aws.amazon.com/)
- [AWS Free Tier](https://aws.amazon.com/free/)
- [nginx doc](https://nginx.org/en/docs/)
- [Hono doc](https://hono.dev/docs/)
