# TaskManager - React Web App Deployment on AWS EC2

## 📝 Project Overview

TaskManager is a cross-platform app built using React and Expo. This repo documents how the **web version** of the app is deployed to an **AWS EC2 Ubuntu instance**, using both:

- **PM2** – to serve the exported static files
- **Docker** – to containerize and run the app

---

## 🖼️ Architecture

- Frontend: Expo (React) Web App
- Deployment: AWS EC2 (Ubuntu)
- Methods:
  - PM2 (serving static files)
  - Docker (containerized Node-based server)

Update packages & install Node.js and npm:
sudo apt update
sudo apt install nodejs npm -y

Clone your repo:
git clone <your-repo-url>
Cd your repo

PM2 Deployment
Step 1: Install PM2 & dependencies
sudo npm install -g pm2 serve
npm install

Step 2: Export the Expo web build
npx expo export
A Dist folder will be created 

Step 3: Serve the app on port 80 with PM2
pm2 serve dist 80 --name TaskManager

step 4: list the running projects
pm2 list

<img width="1352" height="699" alt="Screenshot 2025-08-21 122337" src="https://github.com/user-attachments/assets/754a630b-e060-46b9-b135-a7cb296f7500" />







🐳 Docker Deployment
Step 1: Install Docker
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker

cloned the project form the github the docker file is already present in the project 

Step 2: Build the Docker Image
docker build -t taskmanger .

Step 3: Run the Container
docker run -d -p 3000:80 taskmanager

To see the running containers 
docker ps



