


# Real-Time Chat Application


Welcome to the **Full Stack Realtime Chat App** project, where we're building a scalable and secure real-time chat experience using the latest technologies. Whether you're a seasoned developer or a beginner, we invite you to contribute and be a part of this exciting journey!

## Table of Contents


* [Introduction](#introduction)
* [Features](#features)
* [Tech Stack](#tech-stack)
* [Getting Started](#getting-started)
* [Building the Backend](#building-the-backend)
* [Running the Application](#running-the-application)
* [Contributing](#contributing)
* [Future Plans](#future-plans)
* [License](#license)

## 📝 Introduction

This project aims to provide a real-time chat experience that's both scalable and secure. With a focus on modern technologies, we're building an application that's easy to use and maintain.

## ✨ Features


* **Real-time Messaging**: Send and receive messages instantly using Socket.io 
* **User Authentication & Authorization**: Securely manage user access with JWT 
* **Scalable & Secure Architecture**: Built to handle large volumes of traffic and data 
* **Modern UI Design**: A user-friendly interface crafted with React and TailwindCSS 
* **Profile Management**: Users can upload and update their profile pictures 
* **Online Status**: View real-time online/offline status of users 


## 🛠️ Tech Stack


* **Backend:** Node.js, Express, MongoDB, Socket.io
* **Frontend:** React, TailwindCSS
* **Containerization:** Docker
* **Orchestration:** Kubernetes (planned)
* **Web Server:** Nginx
* **State Management:** Zustand
* **Authentication:** JWT
* **Styling Components:** DaisyUI


### 🔧 Prerequisites


* **[Node.js](https://nodejs.org/)** (v14 or higher)
* **[Docker](https://www.docker.com/get-started)** (for containerizing the app)
* **[Git](https://git-scm.com/downloads)** (to clone the repository)


### 📝 Environment Configuration

Create a `.env` file in the root directory with the following configuration:

```env
# Database Configuration
MONGODB_URI=mongodb://root:admin@mongo:27017/chatApp?authSource=admin&retryWrites=true&w=majority

# JWT Configuration
JWT_SECRET=your_jwt_secret_key

# Server Configuration
PORT=5001
NODE_ENV=production
```

> **Note:** 
> - Replace `your_jwt_secret_key` with a strong secret key
> - For local development without Docker, change `MONGODB_URI` to `mongodb://localhost:27017/chatApp`
> - You can use command ```echo "Text what you want" | base64

### Clone the Repository

```bash
https://github.com/PrajwalBambulkar/ChatApplication.git
```

🏗️ Build and Run the Application

Follow these steps to build and run the application:

1. Build & Run the Containers:

```bash
cd ChatApplication
```
```bash
docker-compose up -d --build
```

2. Access the application in your browser:

```
http://localhost
```
---

## 🛠️ Getting Started

Follow these simple steps to get the project up and running on your local Host using docker.

```bash
https://github.com/PrajwalBambulkar/ChatApplication.git
```

```bash
cd ChatApplication
```
## Create a Docker network:

```bash
docker network create full-stack
```

## 🛠️ Building the Frontend

```bash
cd frontend
```

```bash
docker build -t full-stack_frontend .
```

### Run the Frontend container:

```bash
docker run -d --network=full-stack  -p 5173:5173 --name frontend full-stack_frontend:latest
```
#### The frontend will now be accessible on port 5173.


## Run the MongoDB Container:

```bash
docker run -d -p 27017:27017 --name mongo mongo:latest
```
---

## 🛠️ Building the Backend

```bash
cd backend
```

### Build the Backend image:

```bash
docker build -t full-stack_backend .
```

### Run the Backend container:

```bash
docker run -d --network=full-stack --add-host=host.docker.internal:host-gateway -p 5001:5001 --env-file .env full-stack_backend
```
#### This will build and run the backend container, exposing the backendAPI on port 5001.

`Backend API: http://localhost:5001`

### To Verify the conncetion between backend and databse:
```bash
docker-compose logs -f
```

### Once the backend and frontend containers are running, you can access the application in your browser:

`Frontend: http://localhost`


You can now interact with the real-time chat app and start messaging!

---



### 🤝 Contributing


We welcome contributions from DevOps & Developer of all skill levels! Here's how you can contribute:

**Report bugs:** If you encounter any bugs or issues, please open an issue with detailed information.
**Suggest features:** Have an idea for a new feature? Open an issue to discuss it with the community.
**Submit pull requests:** If you have a fix or a feature you'd like to contribute, submit a pull request. Ensure your changes pass any linting or tests, if applicable.

### 🌐 Join the Community

We invite you to join our community of developers and contributors. Let's work together to build an amazing real-time chat application!

* **Star this repository** to show your support
* **Fork this repository** to contribute to the project
* **Open an issue** to report bugs or suggest features
* **Submit a pull request** to contribute code changes

## 🔮 Future Plans


This project is evolving, and here are a few exciting things on the horizon:

* [ ] **CI/CD Pipelines:** Implement Continuous Integration and Continuous Deployment pipelines to automate testing and deployment.
* [ ] **Kubernetes (K8s):** Add Kubernetes manifests for container orchestration to deploy the app on cloud platforms like AWS, GCP, or Azure.
* [ ] **Feature Expansion:** Add more features like group chats, media sharing, and user status updates.
* **Stay tuned for updates as we continue to improve and expand this project!**

---

## 📚 Project Snapshots:

<img width="1890" height="1051" alt="image" src="https://github.com/user-attachments/assets/da27c690-6599-4bac-a3ed-626ef4b4fa14" />
<img width="1893" height="1041" alt="image" src="https://github.com/user-attachments/assets/43a00e72-4865-478a-985f-e952bbdebbf0" />
<img width="1881" height="1054" alt="image" src="https://github.com/user-attachments/assets/45784373-f0bb-449b-b7fa-587b4f6498e8" />




# Deployment steps for Kubernetes are documented in the k8s/README.md file.















