🚀 GitHub Project: AWS EC2 Complete Guide (Beginner Friendly)

📌 1. Project Title
AWS EC2 Server Setup with Scenario-Based Configuration

📖 2. Definition (Simple + Technical)
Amazon EC2 (Elastic Compute Cloud) is a cloud service that allows you to create virtual servers (instances) on demand.

👉 In simple words:
EC2 = Virtual Computer in Cloud

🎯 3. Real-Time Scenario

Imagine:

👉 You want to host a website
👉 Users from anywhere should access it
👉 Server should run 24/7

Solution:

Launch EC2 instance
Install web server (Apache/Nginx)
Allow HTTP traffic
Access via public IP

🏗️ 4. Architecture Overview
EC2 Instance (Server)
Security Group (Firewall)
Key Pair (Login access)
Internet Gateway (Public access)

🪜 5. Step-by-Step Configuration (Latest AWS Console)

🔹 Step 1: Login to AWS
Go to AWS Console
Search: EC2

🔹 Step 2: Launch Instance

Click Launch Instance
Name: my-ec2-instance-test

🔹 Step 3: Choose AMI
Select: Amazon Ubuntu

👉 Why?
Lightweight + Free tier + Easy setup

🔹 Step 4: Choose Instance Type
Select: t3.micro (Free Tier)

🔹 Step 5: Create Key Pair

Click Create Key Pair
Key pair Name : mytestkey@123
Type: RSA
Format: .pem
Download file

👉 This file is used to login (VERY IMPORTANT)

🔹 Step 6: Configure Network
Allow:
SSH (22) → Your IP
HTTP (80) → Anywhere

🔹 Step 7: Launch Instance
Click Launch Instance

🔹 Step 8: Connect to EC2


Command:
ssh -i "europecdec52.pem" ubuntu@56.228.12.193

🔹 Step 9: Install Web Server
#!/bin/bash
sudo apt update -y
sudo apt install nginx -y
echo "<h1> HelloWorld Form $HOSTNAME</h1>" > /var/www/html/index.html
sudo systemctl start nginx
sudo systemctl enable nginx

🔹 Step 10: Test Website


👉 Open browser:

http://<public-ip>

You will see Apache Test Page ✅
