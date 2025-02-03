# Maven Integration with DockerHub and jenkins #
## Author: Chrisjoel ##

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
