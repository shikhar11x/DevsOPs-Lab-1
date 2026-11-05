# DevOps Lab 1 – Observations

## 1. Environment Setup
- Ubuntu 24.04 LTS was used as the development environment.
- Git was installed and configured for version control.
- Java JDK was installed to support Jenkins.
- Visual Studio Code was used for editing project files.

## 2. Git and GitHub
- A Git repository was initialized for the project.
- Source code and configuration files were tracked using Git.
- Changes were committed with meaningful commit messages.
- The project was pushed to a GitHub remote repository.

## 3. Jenkins Configuration
- Jenkins was installed and configured successfully.
- Jenkins was accessed through the local web interface.
- A Pipeline job was created using the GitHub repository.
- The Jenkinsfile was used to define the CI/CD workflow.

## 4. Pipeline Execution
The pipeline was divided into the following stages:

1. **Checkout:** Retrieved source code from the GitHub repository.
2. **Build:** Checked the required application files.
3. **Test:** Verified the expected content in the HTML and CSS files.
4. **Deploy:** Copied application files to the Nginx web server directory.

## 5. Automation
- Jenkins was configured to monitor repository changes using SCM polling.
- New commits pushed to GitHub can trigger an automated pipeline build.

## 6. Key Learnings
- Understood the fundamentals of DevOps and Continuous Integration.
- Learned how Git and GitHub support source code management.
- Understood how Jenkins automates pipeline execution.
- Learned how to define pipeline stages using a Jenkinsfile.
- Understood the basic process of deploying a web application using Nginx.
- Learned the importance of maintaining a clean commit history.

## Result

Successfully implemented a basic CI/CD workflow using Ubuntu, Git, GitHub, Jenkins, and Nginx. The project demonstrates source code management, automated build and testing checks, and web application deployment.