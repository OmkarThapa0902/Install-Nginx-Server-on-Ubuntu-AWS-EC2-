# Install-Nginx-Server-on-Ubuntu-AWS-EC2

## Complete Step-by-Step Guide
This guide provides detailed instructions for setting up an Nginx web server on an Ubuntu EC2 instance hosted on AWS. Following these steps will allow you to deploy a basic web server, access it via your browser, and ensure it runs on system startup.
### Step 1: Launch an EC2 Instance

1. Go to the EC2 Console.
2. Click **Launch Instance**.
3. Choose **Ubuntu Server 22.04 LTS**.
4. Instance type: **t2.micro (Free Tier)**.
5. Create/Select a **Key Pair**.
6. Configure **Security Group**:

   * Allow **SSH (22)** from your IP.
   * Allow **HTTP (80)** from anywhere.
7. Launch the instance.

---

### Step 2: Connect to the Instance via SSH

Open terminal (Mac/Linux) or PowerShell (Windows):

```bash
ssh -i your-key.pem ubuntu@YOUR_PUBLIC_IP
```

---

### Step 3: Update System Packages

```bash
sudo apt update -y
sudo apt upgrade -y
```
![Step 1 Screenshot](1.png)
---


### Step 4: Install Nginx

```bash
sudo apt install nginx -y
```

---

### Step 5: Start and Enable Nginx

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

### Step 6: Verify Nginx Installation

Check service:

```bash
sudo systemctl status nginx
```
![Step 2 Screenshot](2.png)
---

### Step 7: Test in Your Browser

Go to:

```
http://YOUR_PUBLIC_IP
```

You should see the default **Nginx Welcome Page**.
![Step 3 Screenshot](3.png)
Your Nginx server is now running successfully.
