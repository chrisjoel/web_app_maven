# Maven Integration with DockerHub and jenkins #
## Author: Chrisjoel ##


## About it ##
Jenkins: Acts as the central orchestration server for the CI/CD pipeline. Jenkins automates the execution of various stages defined in the Jenkinsfile.

Maven: Handles building the project, managing dependencies, and running tests. Maven ensures that the application is built correctly and tested before proceeding to the next stages.

GitHub: Hosts the source code repository. Developers commit their code changes here. The repository triggers Jenkins to start the pipeline whenever new changes are pushed.

Docker: Builds a container image of the application. Docker ensures that the application runs consistently across different environments by packaging it with all its dependencies.

Trivy: Scans the Docker image for vulnerabilities. Trivy identifies any critical security issues that need to be addressed before deploying the application.

SonarCloud: Performs static code analysis to ensure code quality and adherence to coding standards. SonarCloud provides insights into code maintainability, reliability, and security.

DockerHub: Hosts the Docker images. After the image is built and scanned, it is pushed to DockerHub, where it can be accessed for deployment.



## Prerequisites ##
1. **Jenkins**: Ensure you have Jenkins installed and running. Follow the installation instructions [here](https://www.jenkins.io/doc/book/installing/).
2. **Docker**: Install Docker on your Jenkins server. Follow the installation guide [here](https://docs.docker.com/get-docker/).
3. **Trivy**: Install Trivy for Docker image scanning. Follow the installation steps [here](https://aquasecurity.github.io/trivy/v0.22.0/installation/).
4. **SonarCloud**: Set up an account on [SonarCloud](https://sonarcloud.io/) and create a project. Make sure you have the `sonarcloud_credential` available in Jenkins credentials.




## Environment Variables ##

- **DOCKER_CREDENTIALS_ID**: Jenkins credentials ID for DockerHub.
- **DOCKER_USERNAME**: DockerHub username.
- **DOCKER_IMAGE**: Name of the Docker image.
- **DOCKER_TAG**: Tag for the Docker image (e.g., `latest`).
- **SONAR_PROJECT_KEY**: SonarCloud project key.
- **SONAR_ORG**: SonarCloud organization.
- **SONAR_TOKEN**: Jenkins credentials for SonarCloud token.



## Architecture ##


![web_app_maven image](https://github.com/user-attachments/assets/20733d73-31ac-4443-ba79-2fa89e0e2df6)
