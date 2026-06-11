# AWS EC2 Nginx Portfolio Deployment Project

## Project Overview

This project demonstrates the deployment of a personal portfolio website on an AWS EC2 Ubuntu Server using a custom VPC architecture and Nginx web server. The project showcases fundamental Cloud Computing, Networking, Linux Administration, AWS Infrastructure, and Git/GitHub skills.

The objective of this project is to create a highly available and secure environment for hosting a static portfolio website while following cloud deployment best practices.

---

## Project Objectives

* Create a Custom VPC
* Create and Configure Public Subnet
* Configure Internet Gateway and Route Tables
* Launch Ubuntu EC2 Instance
* Configure Security Groups
* Install and Configure Nginx
* Deploy Personal Portfolio Website
* Manage Source Code using Git and GitHub
* Document Deployment Process
* Perform Basic Troubleshooting

---

↓

Internet Gateway

↓
Custom VPC

↓

Public Subnet

↓
Security Group

↓
EC2 Ubuntu Server

↓
Nginx Web Server

↓

Portfolio Website


---


## AWS Services Used


* Amazon VPC
* Public Subnet

* Internet Gateway
* Route Table

* Security Group
* Amazon EC2

* Elastic IP (Optional)

---


## Software and Tools Used

* Ubuntu Server

* Nginx
* Git
* GitHub
* Git Bash / Linux Terminal
* AWS Management Console

---

## Deployment Steps

### Step 1: Create Custom VPC

* Create a VPC with your preferred CIDR block.
* Example: 10.0.0.0/16

### Step 2: Create Public Subnet

* Create a Public Subnet.
* Example: 10.0.1.0/24

### Step 3: Create Internet Gateway

* Create Internet Gateway.
* Attach it to the VPC.

### Step 4: Configure Route Table

* Add Route:

  * Destination: 0.0.0.0/0

  * Target: Internet Gateway


### Step 5: Create Security Group


* HTTP (80)
Allow:


* SSH (22)

* HTTPS (443)


### Step 6: Launch Ubuntu EC2 Instance


* Select Ubuntu Server
* Select Security Group

* Select Key Pair


### Step 7: Connect Using SSH


```bash
chmod 400 mykey.pem


ssh -i mykey.pem ubuntu@<Public-IP>

```

### Step 8: Install Nginx


```bash

sudo apt update


sudo apt install nginx -y


sudo systemctl enable nginx


sudo systemctl start nginx
```


### Step 9: Verify Nginx Status


```bash
sudo systemctl status nginx
```


### Step 10: Deploy Website Files


```bash

cd /var/www/html


sudo rm index.nginx-debian.html


sudo nano index.html
```


Paste portfolio website code.


### Step 11: Verify Website


Open browser:


```text
http://<Public-IP>
```

Portfolio website should be accessible.

---

## Git and GitHub Commands Used

### Configure Git

```bash
git config --global user.name "Your Name"

git config --global user.email "yourmail@example.com"
```

### Clone Repository

```bash
git clone <repository-url>
```

### Check Status

```bash
git status
```

### Add Files

```bash
git add .
```

### Commit Changes

```bash
git commit -m "Initial Project Commit"
```

### Push Code

```bash
git push origin main
```

---

## Screenshots Required

Students must attach screenshots of:

* VPC Creation
* Subnet Creation
* Route Table
* Internet Gateway
* Security Group Rules
* EC2 Running State
* SSH Login
* Nginx Installation
* Website Running
* GitHub Repository

---

## Troubleshooting Performed

### Issue 1

Problem:
SSH Permission Denied (publickey)

Possible Causes:

* Wrong Key Pair
* Wrong Username
* Incorrect File Permissions

Solution:

```bash
chmod 400 mykey.pem
```

Verify:

```bash
ssh -i mykey.pem ubuntu@<Public-IP>
```

---

### Issue 2

Problem:
Website Not Accessible

Cause:

Port 80 blocked in Security Group

Solution:

Allow HTTP (80) traffic.

---

### Issue 3

Problem:
Unable to Access Internet from EC2

Cause:

Route Table not configured properly.

Solution:

Add route:

```text
0.0.0.0/0 → Internet Gateway
```

---

## Learning Outcomes

After completing this project, I was able to:

* Design a custom AWS VPC architecture
* Configure Public Subnets and Route Tables
* Launch and manage EC2 instances
* Secure infrastructure using Security Groups
* Install and configure Nginx
* Deploy a portfolio website
* Use Git and GitHub for version control
* Perform troubleshooting and root cause analysis
* Understand cloud deployment workflows

---

## Future Enhancements

* Add Custom Domain
* Configure HTTPS using Let's Encrypt
* Deploy using Docker
* Automate deployment using Jenkins
* Provision infrastructure using Terraform
* Implement Monitoring using CloudWatch

---

## Author

Name: ______________________

Course: Cloud Application Developer

Center: _____________________

Batch: ______________________

GitHub Profile:

---

LinkedIn Profile:

---

