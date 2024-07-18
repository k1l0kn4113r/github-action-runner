# GitHub Actions Self-Hosted Runner with Docker

This repository contains the configuration files to set up a GitHub Actions self-hosted runner using Docker. The runner is configured to run on an ARM64 architecture and includes necessary dependencies such as Node.js and Git.

## Prerequisites

- Docker
- Docker Compose

## Setup

### Files

- `Dockerfile`: Contains the instructions to build the Docker image with the necessary dependencies and configurations for the GitHub Actions runner.
- `docker-compose.yml`: Defines the service for the GitHub Actions runner.

### Steps to Build and Run the Docker Container

1. **Create a Directory for the Runner:**

   Create a directory for the GitHub Actions runner and navigate into it:

   ```sh
   mkdir github-actions-runner && cd github-actions-runner

2. **Clone the Repository:**

   Clone this repository to your local machine:

   ```sh
   git clone https://github.com/yourusername/your-repo.git .

3. **Adjust the Dockerfile:**

   Edit the Dockerfile to replace the placeholder URL and token with your actual GitHub repository URL and token. For example:

   ```sh
   RUN ./config.sh --url YOUR_REPOSITORY_HERE --token YOUR_TOKEN

4. **Build the Docker Image:**

   Build the Docker image using Docker Compose:

   ```sh
   docker-compose build

5. **Run the Docker Container in Detached Mode:**

   Run the Docker container in the background (detached mode):

   ```sh
    docker-compose up -d

6. **Run the Docker Container in Detached Mode:**

   Go to your GitHub repository settings under Settings > Actions > Runners and verify that your self-hosted runner is listed and idle.

7. **Run the Docker Container in Detached Mode:**

   To list all running containers:

   ```sh
    docker ps
