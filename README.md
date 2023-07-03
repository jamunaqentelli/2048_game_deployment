# Project Name: 2048 Game Deployment with Jenkins

🎮🚀

This project demonstrates the deployment of the popular 2048 game using Jenkins, Docker, and a declarative pipeline.

## Project Structure

- **Dockerfile**: This file contains instructions to build a Docker image for the 2048 game.
- **docker-compose.yml**: This file defines the Docker services required to run the game application.
- **Jenkinsfile**: This file contains the declarative pipeline script to automate the deployment process with Jenkins.
- **README.md**: You are here! This file provides information about the project.

## Prerequisites

Before running this project, make sure you have the following:

- Docker installed on your system.
- Jenkins installed and configured with necessary plugins.

## Usage

To deploy the 2048 game using Jenkins and Docker, follow these steps:

1. Clone the repository:

   ```bash
   git clone <repository-link>
   ```

2. Build the Docker image:

   ```bash
   docker build -t 2048-game .
   ```

3. Run the Docker container using Docker Compose:

   ```bash
   docker-compose up -d
   ```

   The game will be accessible at `http://<your-server-ip>:80`.

## Jenkins Pipeline

The project includes a declarative Jenkins pipeline script (`Jenkinsfile`) that automates the deployment process. The pipeline consists of the following stages:

1. **Clone**: Clones the repository if the repository directory does not exist.
2. **Build**: Builds the Docker image for the 2048 game.
3. **Deploy**: Stops and removes any existing containers, and runs a new container with the game.
4. **Test**: Verifies the deployment by making a GET request to the game application and checking if it contains "2048".

To set up the pipeline in Jenkins:

1. Create a new Jenkins pipeline job.
2. Configure the pipeline script with the content of the `Jenkinsfile`.
3. Save the pipeline configuration.
4. Run the pipeline job to deploy the game.

For detailed instructions on setting up Jenkins and running the pipeline, refer to the [blog post](https://dhananjaykulkarni.hashnode.dev/jenkins-declarative-pipeline-deploying-and-automating-the-2048-game).

## Conclusion

Deploying the 2048 game using Jenkins and Docker showcases the power of automation in continuous integration and delivery. The combination of Jenkins' declarative pipeline, Docker's containerization, and the popular game creates an engaging project to explore CI/CD concepts.

For more information, refer to the individual files in the project repository.

🌟 Enjoy playing the 2048 game and exploring the wonders of CI/CD with Jenkins! 🌟
