# 🚀 DevOps Portfolio Project – End-to-End Deployment

![CI/CD](https://img.shields.io/badge/CI%2FCD-Automated-blue)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![AWS](https://img.shields.io/badge/AWS-EC2-orange)
![Netlify](https://img.shields.io/badge/Hosting-Netlify-green)
![Status](https://img.shields.io/badge/Status-Production-success)

---

## 🌍 Live Demo

👉 https://andrescepeda.dev

---

## 🧠 Project Overview

This project demonstrates a complete end-to-end DevOps workflow, starting from infrastructure provisioning on AWS EC2 to production deployment using a CI/CD pipeline with GitHub and Netlify.

The project includes:
- Backend deployment using Flask + Gunicorn
- Reverse proxy configuration with NGINX
- Containerization using Docker
- CI/CD pipeline using GitHub + Netlify
- Domain configuration and HTTPS setup

---

## 🏗️ Architecture
Git → GitHub → Netlify → Internet (CDN + HTTPS)
---

## ⚙️ Tech Stack

- **Cloud**: AWS EC2
- **Backend**: Flask
- **Web Server**: NGINX
- **WSGI Server**: Gunicorn
- **Containerization**: Docker + Docker Compose
- **Version Control**: Git + GitHub
- **CI/CD**: Netlify
- **DNS & Domain**: Namecheap
- **Security**: HTTPS (Let's Encrypt)

---

## 🔧 Project Setup (AWS Phase)

### 1. Connect to EC2
ssh -i key.pem ec2-user@YOUR_IP

2. Install NGINX
sudo yum update -y
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx

3. Run Flask App
python3 app.py

4. Run with Gunicorn
gunicorn --bind 127.0.0.1:5000 app:app

🐳 Dockerization
Build and Run Containers
docker-compose up -d --build

Debugging
docker ps
docker logs flask_app
docker logs nginx_proxy

🔁 CI/CD Deployment (Netlify)
This project uses Netlify for automatic deployments.
Every push triggers:
git push → GitHub → Netlify → Deploy ✅

🌐 Domain & DNS Setup
Configured in Namecheap:

🔒 HTTPS

Enabled using Let's Encrypt (Netlify)
Automatic certificate provisioning
HTTPS enforced with redirect

🚧 Challenges & Solutions
🔴 502 Bad Gateway

Cause: Gunicorn not running
Fix: Restarted service

🔴 Address already in use

Cause: Port conflict
Fix:
sudo pkill gunicorn

🔴 Netlify 404 error

Cause: index.html in wrong folder
Fix:
mv templates/index.html .

🚀 Deployment Workflow
git add .
git commit -m "update"
git push
✔ Automatically triggers deployment on Netlify

💼 Skills Demonstrated
Linux Server Administration
AWS EC2 Deployment
NGINX Reverse Proxy
Gunicorn (WSGI)
Docker & Containerization
Git & GitHub Workflow
CI/CD Pipelines
DNS Configuration
Domain Management
HTTPS / SSL Configuration

🎯 Interview Summary

Designed and deployed a full-stack web application using AWS EC2, containerized services with Docker, and implemented a CI/CD pipeline using GitHub and Netlify. Configured custom domain routing, DNS records, and automatic HTTPS provisioning.

👨‍💻 Author
Andres Cepeda
DevOps Engineer (In Progress 🚀)
LinkedIn: (add your link here)
GitHub: (add your profile link)
