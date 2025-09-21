# Microservices Project

This repository is a **super repo** containing multiple Spring Boot microservices, managed as **Git submodules**. The project uses **Eureka Service Registry** for service discovery.

---

## 🗂 Services Included

| Service Name      | Description                              |
|------------------|------------------------------------------|
| `auth-service`    | Handles user authentication and JWT tokens. |
| `gateway-service` | API Gateway to route requests to backend services and handle JWT validation. |
| `school-service`  | Manages school-related data.             |
| `student-service` | Manages student-related data.            |

---

## ⚙️ Tech Stack

- **Spring Boot** - Java microservices framework  
- **Spring Cloud Netflix Eureka** - Service registry for discovery  
- **Spring Cloud Gateway** - API Gateway for routing and security  
- **JWT** - Authentication tokens  
- **Git Submodules** - Each service maintains its own repo  
- **Maven** - Build tool  

---

## 📂 Repo Structure

microservices-superrepo/
- ├── auth-service/ # Submodule: Auth microservice
- ├── gateway-service/ # Submodule: Gateway microservice
- ├── school-service/ # Submodule: School microservice
- ├── student-service/ # Submodule: Student microservice
- └── README.md

---

## 🚀 How to Clone

Clone the super repo along with all submodules:

```bash
git clone [<super-repo-url>](https://github.com/pasanchamikara99/microservice-super-repo.git)
git submodule update --init --recursive
```
---

## 🏃 Running the Project

1. Start the **Eureka Service Registry** (if it runs as a separate service).  

2. Start each microservice in the following order (or let Eureka register them automatically):  
   1. `auth-service`  
   2. `gateway-service`  
   3. `school-service`  
   4. `student-service`  

3. Access the services via the **Gateway**. Example:

```bash
http://localhost:8080/schools
```

