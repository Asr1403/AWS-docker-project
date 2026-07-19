# Docker Task 2 – Containerization Using Docker

## Project Overview

This project demonstrates how to containerize a simple HTML web application using Docker and deploy it on a cloud virtual machine.

## Project Files

```
task-2/
│── Dockerfile
│── index.html
└── README.md
```

## Technologies Used

- Docker
- Nginx
- HTML
- GitHub

## Dockerfile

```dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
```

## Build Docker Image

```bash
docker build -t task-2 .
```

## Run Docker Container

```bash
docker run -d -p 8080:80 --name task2 task-2
```

## View the Application

Open your browser and visit:

```
http://localhost:8080
```

## Stop the Container

```bash
docker stop task2
```

## Remove the Container

```bash
docker rm -f task2
```

## Cloud Deployment

The Docker container can be deployed on a cloud virtual machine (AWS EC2/Oracle Cloud) by:

1. Launching an Ubuntu VM.
2. Installing Docker.
3. Copying the project files to the VM.
4. Building the Docker image.
5. Running the container on port 80.
6. Accessing the application using the VM's public IP address.

## Author

**Ayush Singh Rajput**

Cloud Computing & DevOps – Task 2
