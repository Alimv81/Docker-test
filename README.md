# Python Project with TensorFlow and OpenCV

This project demonstrates a simple setup using Docker to create a Python environment with TensorFlow and OpenCV libraries. The project includes a basic Python script that imports these libraries and prints their versions.

## Table of Contents

- [Python Project with TensorFlow and OpenCV](#python-project-with-tensorflow-and-opencv)
  - [Table of Contents](#table-of-contents)
  - [Prerequisites](#prerequisites)
  - [Getting Started](#getting-started)
  - [Running the Application](#running-the-application)
  - [Project Structure](#project-structure)
    - [main.py](#mainpy)
  - [Docker Ignore](#docker-ignore)

## Prerequisites

- [Docker](https://www.docker.com/get-started) must be installed on your system.
- A terminal or command prompt to run the Docker commands.

## Getting Started

1. **Clone the repository** or download the project files to your local machine.

2. **Navigate to the project directory**:
   ```bash
   cd "D:\vscode resp\dokcer testing"
   ```

3. **Build the Docker image**:
   ```bash
   docker build -t my-python-app .
   ```

## Running the Application

Once the image is built, you can run the application using:

```bash
docker run -p 5000:5000 my-python-app
```

This command starts the application and maps port 5000 of the container to port 5000 on your local machine.

## Project Structure

```
D:\vscode resp\dokcer testing
│
├── Dockerfile         # Dockerfile for building the Docker image
├── .dockerignore      # Files and directories to ignore when building the image
├── main.py            # Python script that imports TensorFlow and OpenCV
├── requirements.txt   # List of required Python packages
└── useless-file.txt   # A sample file to demonstrate .dockerignore usage
```

### main.py

The `main.py` file contains the following code:

```python
import tensorflow as tf
import cv2

print(cv2.__version__)
print(tf.__version__)
```

When executed, this script will print the versions of the installed TensorFlow and OpenCV libraries.

## Docker Ignore

The `.dockerignore` file prevents certain files from being included in the Docker image, keeping it lightweight. In this project, `useless-file.txt` is ignored during the Docker build process.