# High Availability Web App on AWS EC2  

## Overview  
This project demonstrates hosting a simple web application on AWS EC2 with high availability using AMI, Load Balancer, and Auto Scaling.  

## Steps Implemented  

### 1. Launch First EC2 Instance  
- Created `web-server-1` on Amazon Linux 2.  
- Installed Nginx and deployed `index.html`.  
- Verified in browser with public IP.  

### 2. Create Custom AMI & Launch Second Instance  
- Created AMI `web-server-ami`.  
- Launched `web-server-2` from AMI.  
- Verified webpage loads successfully.  

### 3. Configure Application Load Balancer (ALB)  
- Created Target Group `web-target-group`.  
- Registered both instances.  
- Created ALB `web-alb` and attached target group.  
- Verified DNS distributes traffic between servers.  

### 4. Configure Auto Scaling Group (ASG)  
- Created Launch Template `web-launch-template` (based on AMI).  
- Created ASG `web-asg` with min=2, desired=2, max=4.  
- Attached ASG to ALB.  
- Tested: stopping an instance → ASG auto launched a new one.  

## Key Learnings  
- EC2 provisioning and SSH connection.  
- Web server deployment on AWS.  
- AMI creation for scaling.  
- Load balancing with ALB.  
- Automatic scaling with ASG.  
