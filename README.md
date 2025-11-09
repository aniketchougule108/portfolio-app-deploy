# 🌐 Portfolio Website — CI/CD Automation (DevOps Project)
## Aniket Chougule - Portfolio

### 🚀 Overview
* A fully automated deployment pipeline for a static Portfolio Website using **GitHub → Jenkins → AWS EC2 → Nginx** Web Server.
* This project demonstrates practical DevOps implementation including Continuous Integration, Continuous Deployment, Cloud Hosting, and Infrastructure Automation.

---

### ⚡ Architecture Diagram

![](./img/architecture.png)
---
### 🧩 Tech Stack
<table border="1" cellspacing="0" cellpadding="8">
  <tr>
    <th>Tool/Service</th>
    <th>Purpose</th>
  </tr>
  <tr>
    <td><strong>Git</strong></td>
    <td>Source code tracking</td>
  </tr>
  <tr>
    <td><strong>GitHub</strong></td>
    <td>Cloud repository + Webhooks</td>
  </tr>
  <tr>
    <td><strong>Jenkins</strong></td>
    <td>CI/CD Pipeline Automation</td>
  </tr>
  <tr>
    <td><strong>AWS EC2 (Ubuntu)</strong></td>
    <td>Web Hosting Server</td>
  </tr>
  <tr>
    <td><strong>Nginx</strong></td>
    <td>Static website hosting</td>
  </tr>
  <tr>
    <td><strong>SSH Key Authentication</strong></td>
    <td>Secure deployment</td>
  </tr>
</table>

---

### 🔁 Workflow Summary

✅ Developer pushes code → GitHub  
✅ Jenkins automatically pulls latest code  
✅ Nginx server auto-deploys new version  
✅ Site updated instantly with no manual steps 

---

### ⚙️ Project Workflow – Step by Step Explanation
✅ 1️⃣ Development – Local System  
* Static Portfolio Website using HTML + CSS
* Verified via VS Code Live Server

💡 Code Structure:
```
PORTFOLIO-APP-CI-CD/
│── index.html
│── css/
│── images/
│── Jenkinsfile

```
---

### ✅ 1. Create GitHub Repo
Create a repository on Github Name: `portfolio-app-deploy-jenkins-CICD` Branch: main

![](./img/github%20Screenshot.png)
---

### 🧰 2. Initialize Git and Push Code to GitHub 
sed Git to version control and push code to GitHub.

```
git init
git add .
git commit -m "Initial portfolio upload"
git branch -M main
git remote add origin https://github.com/aniketchougule108/portfolio-app-deploy.git
git push -u origin main
````
![](./img/push%20Screenshot.png)

✅ After this, the complete project (HTML, CSS, images, Jenkinsfile) is available publicly on GitHub.
👉 GitHub Repository

---

### ✅ 3. Jenkins Credentials
**Manage Jenkins → Credentials → System → Global:**

* Create New Credentails
     * Scope: `Global`
     * id: `node-app-key`
     * description: `node-app-key`
     * username: `ubuntu`
     * private key: `Your-Private-Key`

![](./img/cred%20Screenshot.png)
---
### ✅ 4. Setup Portfolio EC2 (Srver 2)

* Launch a new Ubuntu EC2 instance for portfolio hosting.
* Open inbound port 80 (HTTP) in AWS Security Group.
* Jenkins pipeline will handle Nginx installation automatically.

![](./img/Server%20Screenshot.png)

---

### 🔁 5. Jenkins Pipeline Configuration
In Jenkins Dashboard:

* Create a new Pipeline Project → `portfolio-deploy`
* Select “Pipeline Script from SCM”
* SCM: Git
* Repo URL: `https://github.com/aniketchougule108/Portfolio-app-deploy-Jenkins-CICD.git`
* Branch: `main`
* Script Path: `Jenkinsfile`

![](./img/job%20Screenshot.png)

![](./img/build%20screenshot.png)
---

### 🧾 Jenkinsfile (CI/CD Pipeline Script)

![](./img/jenkinsfile%20Screenshot.png)
---

### 🌍 Live Deployment
🚧 Deployment ready on AWS EC2 – Coming soon!

![](./img/Screenshot%20(256).png)

![](./img/Screenshot%20(250).png)

![](./img/Screenshot%20(242).png)
---

### ✅ Key Highlights
* Fully automated CI/CD using Jenkins
* Zero manual deployment — push → auto-update
* Secure & scalable AWS setup
* Separate Jenkins and Deployment EC2 servers
* Nginx as production-grade static web host
---
### 🏁  Conclusion :
As a dedicated Cloud & DevOps Enthusiast, I am continuously learning modern tools and technologies to improve automation, scalability, and efficient deployment. I am eager to contribute my skills to real-world projects and grow into a highly skilled Cloud & DevOps professional.
