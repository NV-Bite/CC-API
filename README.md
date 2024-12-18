# CC API NV BITE

This repository contains the API layer and the cloud infrastructure, which work together to support all the main features and functionalities of the project, ensuring it runs smoothly and efficiently.

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Tools](#tools)
- [API Documentation](#api-documentation)
  - [Authentication](#authentication)
  - [Machine Learning Endpoints](#machine-learning-endpoints)
  - [User Management Endpoints](#user-management-endpoints)
- [Cloud Architecture](#cloud-architecture)
- [License](#license)

---

## Introduction

NV-Bite leverages machine learning, cloud computing, and modern web development tools to build a sustainable application. The main goals are:

- Classifying food-related data to estimate carbon footprints.
- Integrating with cloud platforms for scalability and performance.
- Delivering accessible APIs for seamless integration.

---

## Features

- **Machine Learning Integration**: APIs for predictive analytics based on food carbon footprints.
- **Cloud Deployment**: Hosted on Google Cloud Platform for scalability.
- **Comprehensive Documentation**: API usage guide available via Postman.
- **Modern Tools**: Built with industry-standard technologies like Node.js, Docker, and Firebase.

---

## Installation

Follow these steps to install and run the project locally.

### Prerequisites

Make sure the following tools are installed:

- [Node.js](https://nodejs.org/) (version 14 or above)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Steps to Install and Run

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/NV-Bite/cc-api.git
   cd cc-api
   ```

2. **Install Dependencies**:

   ```bash
   npm install
   ```

3. **Run the Server**:

   ```bash
   npm start
   ```

4. The server will start on `http://localhost:3000` by default.

---

## Tools

The following tools and platforms are used in this project:

- [Google Cloud Platform](https://cloud.google.com/): Cloud hosting and services.
- [Node.js](https://nodejs.org/): Backend runtime environment.
- [Firebase](https://firebase.google.com/): Real-time database and authentication.
- [Docker](https://www.docker.com/): Containerization for consistent deployments.
- [Postman](https://www.postman.com/): API testing and documentation.

---

## API Documentation

### Authentication

#### **User Sign In**

- **Endpoint**: `POST {{url}}/users/signin`
- **Description**: Logs in an existing user.
- **Request Body**:
  ```json
  {
    "email": "testing_deploy@gmail.com",
    "password": "12345678"
  }
  ```

#### **User Sign Up**

- **Endpoint**: `POST {{url}}/users/signup`
- **Description**: Registers a new user.
- **Request Body**:
  ```json
  {
    "email": "testing_deploy@gmail.com",
    "password": "12345678",
    "name": "deploy abis",
    "phoneNumber": "0813132111231"
  }
  ```

### Machine Learning Endpoints

#### **Detect Machine Learning**

- **Endpoint**: `POST {{url}}/machine-learning/upload`
- **Description**: Uploads an image for machine learning detection.
- **Request Form-Data**:
  - **Key**: `image`  
    **Type**: File  
    **Example**: An image file (e.g., `1977343241.jpg`).

#### **Get Machine Learning History**

- **Endpoint**: `GET {{url}}/machine-learning/history`
- **Description**: Retrieves the history of machine learning detections.

### User Management Endpoints

#### **Get Profile Detail**

- **Endpoint**: `POST {{url}}/users/getProfile`
- **Description**: Retrieves detailed user profile information.
- **Request Body**:
  ```json
  {
    "id": "PdEZq6SEzOMAWqoqHy3I9p6wSvD3"
  }
  ```

#### **Update Profile**

- **Endpoint**: `POST {{url}}/users/updateProfile`
- **Description**: Updates user profile information.
- **Request Body**:
  ```json
  {
    "id": "PdEZq6SEzOMAWqoqHy3I9p6wSvD3",
    "name": "si ganteng",
    "photoUrl": "https://www.example.com/photo.jpg"
  }
  ```

---

## Cloud Architecture

The NV-Bite application is designed with a scalable and efficient cloud architecture. Below is the architecture diagram:

<div align="center">
  <img src="https://github.com/NV-Bite/.github/blob/main/assets/cc_image/Diagram%20Cloud%20Architecture.png" alt="Cloud Architecture" style="width: 100%;">
</div>

**Key Components**:

- **Compute**: APIs hosted on Google Cloud Run for serverless and scalable execution.
- **Storage**: Data stored on Google Cloud Storage and Firebase for flexibility and real-time updates.
- **Networking**: Managed networking through GCP for secure and optimized communication.

---

## License

This project is licensed under the [MIT License](LICENSE).

---
