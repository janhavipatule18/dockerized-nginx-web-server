# 🚀 Dockerized NGINX Web Server

## 📌 Project Overview

This project demonstrates how to deploy a static website using **Docker containerization** and the **NGINX web server**.

The website is packaged into a Docker image and deployed inside a Docker container. This makes the application portable, isolated, and easy to manage across different environments.

This project was developed as part of my **DevOps Internship - Task 4: Web Server using Docker**.

---

# 🏗️ Project Architecture

```
Developer
    |
    ↓
HTML Website (index.html)
    |
    ↓
Dockerfile
    |
    ↓
Docker Image
(my-nginx-website)
    |
    ↓
Docker Container
(nginx-website-container)
    |
    ↓
NGINX Web Server
    |
    ↓
Browser Access
(localhost:8081)
```

---

# 🛠️ Technologies Used

- 🐳 Docker
- 🌐 NGINX
- 📄 HTML
- 🐧 Linux

---

# 📂 Project Structure

```
dockerized-nginx-web-server/
│
├── Dockerfile
├── index.html
├── docker-images.png
├── docker-container-management.png
├── docker-container-logs.png
├── nginx-website-output.png
└── README.md
---

# 🐳 Docker Implementation

## 1. Dockerfile

The Dockerfile uses the official NGINX image and copies the custom website into the NGINX web directory.

```dockerfile
FROM nginx:latest

COPY index.html /usr/share/nginx/html/index.html
```
---

# 🚀 Docker Commands Used

## Build Docker Image

```bash
docker build -t my-nginx-website .
```

### Explanation:

- `docker build` creates a Docker image.
- `-t` assigns a name/tag to the image.
- `.` uses the current directory as the build context.

Created image:

```
my-nginx-website:latest
```

---

## Run Docker Container

```bash
docker run -d -p 8081:80 --name nginx-website-container my-nginx-website
```

### Explanation:

- `docker run`
  - Creates and starts a container.

- `-d`
  - Runs the container in detached/background mode.

- `-p 8081:80`
  - Maps host port `8081` to container port `80`.

- `--name`
  - Assigns a custom container name.

- `my-nginx-website`
  - The Docker image used to create the container.

---

## Check Running Containers

```bash
docker ps
```

Used to monitor active Docker containers and verify that the NGINX server is running.

---

## View Container Logs

```bash
docker logs nginx-website-container
```

Used for monitoring and troubleshooting container applications.

---

# 🔄 Container Lifecycle Management

The following Docker commands were used to understand container lifecycle:

## Start Container

```bash
docker start nginx-website-container
```

Starts a stopped container.

---

## Stop Container

```bash
docker stop nginx-website-container
```

Stops a running container.

---

## Remove Container

```bash
docker rm nginx-website-container
```

Removes the container after stopping it.

---

# 🔍 Monitoring and Troubleshooting

Container health and application status were monitored using:

```bash
docker ps
```

Container logs were checked using:

```bash
docker logs nginx-website-container
```

During development, webpage update and character encoding issues were resolved by:

- Updating the HTML file
- Rebuilding the Docker image
- Redeploying the container

This demonstrates basic troubleshooting in a containerized environment.

---

# ✨ Features

✅ Custom Docker image creation  
✅ NGINX web server deployment  
✅ Static website hosting  
✅ Container-based application deployment  
✅ Port mapping configuration  
✅ Container lifecycle management  
✅ Application troubleshooting using Docker logs  

---

# 🌐 Application Output

The deployed website can be accessed using:

```
http://localhost:8081
```

The webpage displays a professional DevOps-themed landing page hosted through an NGINX Docker container.

---

# 📚 Internship Task Coverage

## Task 4: Web Server using Docker

### Objectives Completed:

✅ **Learn Docker containerization basics**
- Created Dockerfile
- Built custom Docker image
- Managed Docker containers

✅ **Deploy and manage a web server inside Docker containers**
- Deployed NGINX web server
- Hosted a custom static website
- Configured port mapping

✅ **Understand container lifecycle and commands**
- Created containers
- Started and stopped containers
- Managed container resources

✅ **Monitor container health and troubleshoot issues**
- Checked container status
- Viewed container logs
- Fixed deployment issues

✅ **Explore container-based application deployment best practices**
- Used official NGINX image
- Used Dockerfile-based deployment
- Created a portable containerized application

---

# 📸 Project Screenshots

Screenshots include:

- Docker image creation
- Running Docker container
- Website output
- Container logs
- Container lifecycle commands

---

# 👩‍💻 Created By

**Janvi**

DevOps Internship Project  
Task 4: Web Server using Docker
