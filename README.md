# Introduction: 

The Octopus Project is a Dockerized React application designed to showcase the best practices in modern web development, containerization, and CI/CD workflows. The project is configured to build and deploy across multiple CPU architectures (amd64 and arm64) using GitHub Actions.

# Features:

Multi-Architecture Support: Build and run the application on both amd64 and arm64 platforms.
Automated CI/CD: Uses GitHub Actions to automate the building and pushing of Docker images.
React Application: A simple yet powerful React application as the core of the project.
Dockerized Setup: Easily deploy and run the application using Docker.

# Building the Docker Image:

To build the Docker image locally, run the following command:

- `docker build -t dinesh0724/octopus:0.0.1.RELEASE .`

# Running the Docker Container:

- `docker run -d -p 3000:3000 dinesh0724/octopus:0.0.1.RELEASE`

# Docker Hub
The Octopus Docker images are available on Docker Hub. You can pull and run the images directly from Docker Hub.

# Pulling the Image
To pull the latest Docker image from Docker Hub, run:

- latest-macos-latest-amd64
  
  `docker pull dinesh0724/octopus:latest-macos-latest-amd64`

- latest-macos-latest-arm64

  `docker pull dinesh0724/octopus:latest-macos-latest-arm64`

- latest-windows-latest-amd64
 
   `docker pull dinesh0724/octopus:latest-windows-latest-amd64`


- latest-windows-latest-arm64

   `docker pull dinesh0724/octopus:latest-windows-latest-arm64`


# Supported Architectures
    This project supports the following architectures:

    * amd64
    * arm64
    
    You can pull architecture-specific images using tags like latest-amd64 or latest-arm64.   



# GitHub Actions Workflow
The GitHub Actions workflow is defined in `.github/workflows/docker-multiarch-build.yml`. It performs the following tasks:

1. Checkout the Code: Retrieves the latest code from the repository.
2. Set up Docker Buildx: Prepares the environment for multi-architecture builds.
3. Log in to Docker Hub: Authenticates with Docker Hub using GitHub Secrets.
4. Build and Push: Builds Docker images for amd64 and arm64 platforms and pushes them to Docker Hub.


# Contributing
Contributions are welcome! If you’d like to contribute to the project, please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch-name`.
3. Make your changes and commit them: `git commit -m 'Add some feature`.
4. Push to the branch: `git push origin feature-branch-name`.
5. Submit a pull request.


