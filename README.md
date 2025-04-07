# nodejs-demo-app
Node.js CI/CD Pipeline with Docker & GitHub Actions
This project demonstrates how to automate the build and deployment process of a simple Node.js web application using GitHub Actions and Docker.

📌 Objective
To set up a CI/CD pipeline that automatically:
Builds a Docker image
Pushes it to DockerHub
Deploys the updated Node.js app

🛠️ Tools & Technologies
Node.js
GitHub & GitHub Actions
Docker & DockerHub

📁 Project Structure
nodejs-demo-app/
├── app.js
├── package.json
├── Dockerfile
└── .github/
    └── workflows/
        └── main.yml
        
🔧 How It Works
CI/CD pipeline is defined in .github/workflows/main.yml
On every push to the main branch:
Code is checked out
Docker is set up
DockerHub login is done using GitHub Secrets
Docker image is built and pushed to DockerHub

🐳 Docker
The app is containerized using a Dockerfile:
Base Image: node:18
Port: 3000
Entry: node app.js

📦 DockerHub Image
You can pull and run the image using:
docker pull reddyjancyparshuram/nodejs-demo-app
docker run -p 3000:3000 reddyjancyparshuram/nodejs-demo-app

✨ Output
When accessed at http://localhost:3000, the app displays:
Hello ElevateLabs, Jancy Parshuram Reddy, and All the Interns from Node.js App with CI/CD!

✅ Status
CI/CD pipeline and Docker image push is fully functional. Project tested and running successfully.
