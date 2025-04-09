# 🚀 Elevate Lab Node.js App

Welcome to **Elevate Lab**, a simple Node.js app deployed using **CI/CD** pipeline with **Jenkins** on **AWS EC2**.  
This project is built and maintained by [Mohammed Faisal Iqbal](https://github.com/faisaliqbal-dev).

---

## 📌 About the Project

This Node.js web app displays a welcome page and is designed to help me learn:

- ✅ CI/CD pipelines using Jenkins  
- ✅ Node.js app deployment on EC2  
- ✅ GitHub integration with Jenkins  
- ✅ Process management using PM2  

---

## 🛠️ Tech Stack

- Node.js  
- Express.js  
- Jenkins  
- GitHub  
- AWS EC2 (Ubuntu)  
- PM2  

---

## 🔁 CI/CD Pipeline Stages (via Jenkins)

1. **Build Stage**  
   Clone the GitHub repo inside Jenkins workspace.

2. **Test Stage**  
   (Optional) Install dependencies using `npm install`.

3. **Deploy Stage**  
   Restart the Node.js app using PM2.

   ```bash
   cd $WORKSPACE
   pm2 delete elevate-app || true
   pm2 start index.js --name elevate-app
🚀 How to Run Locally
git clone https://github.com/faisaliqbal-dev/elevate-app.git
cd elevate-app
npm install
node index.js

Then open:
http://localhost:3000

🧠 What I Learned
Setting up Jenkins on EC2

Creating pipeline jobs (not freestyle)

Using GitHub as SCM

Port opening and security group rules in AWS

Managing Node.js apps with PM2
