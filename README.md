# flask-app-1
## Automatic Docker Image Build and Push with GitHub Actions

This repository contains a simple Flask application that is containerized using Docker. The Docker image is automatically built and pushed to Docker Hub using GitHub Actions. Additionally, a scheduled workflow is set up to trigger a build every Saturday at 7 PM.

### How it works:

1. **Flask Application**: The Flask application is a basic "Hello, World!" example, which is defined in the `app.py` file.

2. **Dockerization**: The Flask application is Dockerized using a `Dockerfile`. This file defines the environment and dependencies required to run the Flask application inside a Docker container.

3. **GitHub Actions Workflow**: The `.github/workflows/docker-build-push.yml` file contains the GitHub Actions workflow definition. This workflow is triggered on every push to the main branch and also runs on a scheduled basis every Saturday at 7 PM. It uses Docker build and push commands to build the Docker image and push it to Docker Hub.

4. **Docker Hub Access Token**: To authenticate with Docker Hub, a Docker access token is stored as a secret named `DOCKER_ACCESS_TOKEN` in the repository settings. This token is used by the GitHub Actions workflow to login to Docker Hub and push the Docker image.

### How to use:

1. Clone this repository to your local machine.
2. Update the Flask application or Dockerfile as needed for your project.
3. Generate a Docker access token from Docker Hub and add it as a secret named `DOCKER_ACCESS_TOKEN` in the repository settings.
4. Commit and push your changes to the main branch.
5. The GitHub Actions workflow will automatically trigger a build and push to Docker Hub on every push to the main branch and also on the scheduled time every Saturday at 7 PM.
