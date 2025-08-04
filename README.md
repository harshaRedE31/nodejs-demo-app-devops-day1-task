Node.js Application with Automated CI/CD Pipeline
This project demonstrates the setup of a complete CI/CD pipeline for a simple Node.js web application using GitHub Actions. The primary objective is to automate the process of building a Docker image and pushing it to Docker Hub whenever new code is pushed to the 

main branch.


🛠️ Tools and Technologies Used

Node.js: The runtime environment for the sample web application.



Docker: Used for containerizing the application.


GitHub: The code repository and platform for the CI/CD pipeline.


GitHub Actions: The automation tool used to create the CI/CD workflow.


Docker Hub: The container registry used for storing the public Docker image.

⚙️ CI/CD Pipeline Workflow
The automation is defined in the 

.github/workflows/main.yml file  and performs the following steps:


Trigger: The workflow is automatically triggered on any push event to the main branch of this repository.

Checkout Code: The first step in the job checks out the repository's code into the runner environment.

Log in to Docker Hub: The pipeline securely logs into Docker Hub using credentials stored as GitHub Secrets.


Build and Push Image: It then proceeds to build a Docker image from the Dockerfile and pushes the newly created image to Docker Hub, tagging it as latest.

🚀 How to Run the Application
Since the CI/CD pipeline automatically deploys the image to Docker Hub, you can run the application with a single Docker command.

Pull the image from Docker Hub:

Replace YOUR_DOCKERHUB_USERNAME with your actual Docker Hub username.

Bash

docker pull YOUR_DOCKERHUB_USERNAME/nodejs-demo-app:latest
Run the container:

This command will start the container and map port 80 on your local machine to port 3000 inside the container.

Bash

docker run -p 80:3000 YOUR_DOCKERHUB_USERNAME/nodejs-demo-app:latest
Access the application:

Open your web browser and navigate to http://localhost. You should see the message "Hello, World!".
