# Makensis / Nsis

## Description
This Git repository contains a Dockerfile that allows you to build a Docker image to make a .exe with *Makensis* on Unix. The generated Docker image will be published on Docker Hub for easy deployment by users and their CI/CD.

## Prerequisites
Before getting started, ensure that the following are installed on your local machine:
- Docker: [Docker installation link](https://docs.docker.com/get-docker/)

## How to use
This Docker image is based on `Ubuntu:jammy`. 
To create an executable you can launch this command into the folder of your .nsis file
`docker run -it -v $(pwd):/app damdam00/makensis bash -c "makensis file.nsis"` 

## Local installation Instructions
Follow the steps below to install and run the application in a Docker container:

1. Clone this Git repository to your local machine:
   ```shell
   git clone https://github.com/your-username/project-name.git
   ```

2. Navigate to the project directory:
   ```shell
   cd project-name
   ```

3. Build the Docker image using the following command:
   ```shell
   docker build -t image-name:tag .
   ```
   Make sure to replace `image-name` and `tag` with your desired values.

4. Once the image building process is complete, you can run a Docker container from this image:
   ```shell
   docker run -p <host-port>:<container-port> image-name:tag
   ```

## Contribution
Contributions to this project are welcome. Here are the steps to contribute:

1. Fork the repository.
2. Create a branch for your modifications:
   ```shell
   git checkout -b my-branch
   ```
3. Make the necessary changes and improvements.
4. Thoroughly test the modifications.
5. Commit the changes:
   ```shell
   git commit -m "Description of the changes"
   ```
6. Push the changes to your fork:
   ```shell
   git push origin my-branch
   ```
7. Open a Pull Request in the original repository.