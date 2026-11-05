# DevOps Lab 1: Foundations & Continuous Integration

## Overview

This project demonstrates the implementation of a foundational DevOps workflow using Git, GitHub, Jenkins, Ubuntu Linux 24.04 LTS, and Nginx.

The objective is to establish version control, configure a Jenkins CI/CD pipeline, automate application build and testing, and deploy the application automatically.

## Objectives

- Understand Git-based version control.
- Create and manage a GitHub repository.
- Install and configure Jenkins.
- Build a CI/CD pipeline using a Jenkinsfile.
- Automate application build and testing.
- Deploy the application using Nginx.
- Maintain meaningful commits and proper documentation.

## Technology Stack

| Technology | Purpose |
|---|---|
| Ubuntu 24.04 LTS | Operating system |
| Git | Version control |
| GitHub | Remote repository |
| Visual Studio Code | Code editor |
| Java 21 | Jenkins runtime |
| Jenkins | CI/CD automation |
| Nginx | Web server |
| HTML5 | Application structure |
| CSS3 | Application styling |

## Project Structure

```text
DevOps-Lab-1/
│
├── index.html
├── style.css
├── Jenkinsfile
├── README.md
├── observations.md
│
└── screenshots/
```

## CI/CD Pipeline Architecture

The project follows this workflow:

1. **Source Control:** Application source code is maintained using Git.
2. **GitHub Repository:** Code is pushed to the remote GitHub repository.
3. **Checkout:** Jenkins retrieves the latest source code.
4. **Build:** Jenkins verifies the required application files.
5. **Test:** Automated checks validate the application files.
6. **Deploy:** Jenkins copies the application files to the Nginx web directory.
7. **Verification:** The deployed application is accessed through localhost.

## Jenkins Pipeline Stages

The Jenkinsfile contains the following stages:

| Stage | Description |
|---|---|
| Checkout | Retrieves source code from GitHub |
| Build | Checks required application files |
| Test | Performs automated content validation |
| Deploy | Deploys files to the Nginx web server |
| Post | Reports pipeline success or failure |

## Installation and Execution

### 1. Update Ubuntu

```bash
sudo apt update
sudo apt upgrade -y
```

### 2. Install Git

```bash
sudo apt install git -y
git --version
```

### 3. Install Java

```bash
sudo apt install openjdk-21-jre -y
java -version
```

### 4. Install Jenkins

Install Jenkins using the official Debian repository instructions:

https://www.jenkins.io/doc/book/installing/linux/

Start Jenkins:

```bash
sudo systemctl enable jenkins
sudo systemctl start jenkins
```

Access Jenkins:

http://localhost:8080

### 5. Configure Git

```bash
git config --global user.name "Shikhar Bajpai"
git config --global user.email "YOUR_GITHUB_EMAIL"
```

### 6. Initialize Repository

```bash
git init
git add .
git commit -m "Initial commit: add sample web application"
git branch -M main
```

### 7. Connect GitHub

```bash
git remote add origin https://github.com/shikhar11x/DevOps-Lab-1.git
git push -u origin main
```

Replace the repository URL if your actual GitHub repository has a different name.

### 8. Install Nginx

```bash
sudo apt install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```

### 9. Run the Pipeline

1. Open Jenkins Dashboard.
2. Create a new Pipeline job.
3. Select Pipeline script from SCM.
4. Choose Git as the source control system.
5. Enter the GitHub repository URL.
6. Set the branch to `*/main`.
7. Set Script Path to `Jenkinsfile`.
8. Save and click Build Now.

## Screenshots and Evidence

Screenshots documenting the experiment are maintained in the `screenshots/` directory.

| Screenshot | Description |
|---|---|
| 01-ubuntu.png | Ubuntu environment |
| 02-git.png | Git configuration |
| 03-java.png | Java installation |
| 04-jenkins.png | Jenkins service |
| 05-dashboard.png | Jenkins dashboard |
| 06-github.png | GitHub repository |
| 07-jenkinsfile.png | Pipeline configuration |
| 08-pipeline.png | Pipeline execution |
| 09-console.png | Jenkins console output |
| 10-deployment.png | Deployed web application |

## Observations

- Git successfully manages application source code.
- GitHub provides remote source code storage.
- Jenkins automates the CI/CD workflow.
- The Jenkinsfile defines reproducible pipeline stages.
- Automated tests validate application files.
- Nginx serves the deployed application.

## Result

Successfully implemented a foundational DevOps CI/CD workflow using Ubuntu Linux 24.04, Git, GitHub, Jenkins, Java, and Nginx.

The project demonstrates version control, automated build and testing, and application deployment through a Jenkins pipeline.

## Author

**Shikhar Bajpai**

B.Tech Computer Science and Engineering

GitHub: https://github.com/shikhar11x
