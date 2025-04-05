# Qubool Kallyaanam: Matrimonial Platform for Muslims in Kerala

**Qubool Kallyaanam** is a dedicated matrimonial platform designed for the Muslim community in Kerala. The project is developed using a microservices architecture, ensuring scalability, flexibility, and maintainability. Initially, the focus is on backend development using Golang, with plans to extend into frontend and mobile app development in the future.

## Table of Contents
- [Project Overview](#project-overview)
- [Architecture](#architecture)
- [Repository Structure](#repository-structure)
- [Technology Stack](#technology-stack)
- [Deployment](#deployment)
- [Roadmap](#roadmap)
- [License](#license)

## Project Overview

Qubool Kallyaanam is being built to offer a secure, reliable, and efficient matrimonial experience for Muslims in Kerala. The platform is designed to facilitate meaningful connections by leveraging a robust backend powered by Golang and a microservices-based architecture.

**Key Features:**
- **User Registration & Profile Management:** Easy onboarding and secure profile management.
- **Authentication & Authorization:** Secure login mechanisms for users and admins.
- **Administration Panel:** Tools for platform management and moderation.
- **Real-time Chat:** Text-based communication between users.

## Architecture

This project follows a microservices architecture to isolate and manage different aspects of the platform. Each service is responsible for a specific functionality, which promotes scalability and easier maintenance.

The core microservices include:
- **API Gateway (`api-gateway-qubool-kallyaanam`):** Acts as the entry point for all client requests and handles routing to the appropriate services.
- **Authentication Service (`auth-service-qubool-kallyaanam`):** Manages user authentication and authorization.
- **User Service (`user-service-qubool-kallyaanam`):** Handles user profiles, registration, and related functionalities.
- **Admin Service (`admin-service-qubool-kallyaanam`):** Provides administrative functions and platform moderation.

## Repository Structure

The root repository serves as an umbrella for the individual microservices, which are included as Git submodules. The structure is as follows:

  .

  ├── LICENSE 

  ├── api-gateway-qubool-kallyaanam 

  ├── auth-service-qubool-kallyaanam 

  ├── user-service-qubool-kallyaanam 

  └── admin-service-qubool-kallyaanam


Each submodule represents a separate microservice with its own repository, allowing independent development and deployment.

## Technology Stack

- **Backend:** Golang
- **Databases:** 
  - PostgreSQL (Relational)
  - MongoDB (NoSQL)
  - Redis (Caching)
- **Containerization & Orchestration:** Docker, Kubernetes
- **Cloud Hosting:** AWS or GCP (to be decided based on requirements and cost analysis)
- **Communication:** Text-based chat implementation

## Deployment

The project is designed to be cloud-native and containerized, ensuring that it can scale efficiently in a cloud environment. The key steps for deployment include:

1. **Dockerize the Services:** Each microservice has its own Dockerfile.
2. **Orchestrate with Kubernetes:** Use Kubernetes for container orchestration, service discovery, and scaling.
3. **Cloud Deployment:** Deploy on AWS or GCP. Configuration files and deployment scripts are provided in the respective microservice repositories.

## Roadmap

1. **Current Focus: Backend Development**
   - Build and refine each microservice using Golang.
   - Set up and configure the databases (PostgreSQL, MongoDB, Redis).
   - Develop API endpoints and integrate the microservices via the API gateway.

2. **Future Enhancements:**
   - **Frontend Development:** Develop a responsive web application.
   - **Mobile App Development:** Implement mobile applications for iOS and Android.
   - **Enhanced Chat Features:** Expand text-based chat capabilities and add more features like notifications.
   - **Additional Services:** Implement further enhancements as per user feedback and evolving requirements.

## License

This project is licensed under the [MIT License](./LICENSE).
