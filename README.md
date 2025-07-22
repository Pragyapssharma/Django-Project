# 🚆 RailSathi Complaint Microservice
RailSathiBE is a FastAPI-based backend microservice designed to handle passenger complaints for Indian Railways. It supports complaint creation, retrieval, updating, deletion, and email notifications — all powered by PostgreSQL and Docker.

## 📦 Tech Stack
- FastAPI RESTful API
- PostgreSQL database integration
- Complaint management (CRUD)
- Email notifications using Gmail SMTP
- Dockerized deployment
- Swagger documentation
- Health check endpoint


## 🚀 Setup Instructions
Prerequisites
- Python 3.9+
- Docker & Docker Compose
- PostgreSQL (local or containerized)

### 1. Clone the Repo
```bash
git clone https://github.com/Pragyapssharma/Django-Project
cd RailSathiBE
```

### 2. Environment Setup

Create a .env file using the provided .env.example

### 3. Run with Docker

```bash
docker-compose up --build
```
Access the app at:
http://localhost:8000

### 4. API Endpoints

PI Endpoints
| Method | Endpoint | Description | 
| GET | /health | Health check | 
| GET | /rs_microservice | Microservice status | 
| POST | /rs_microservice/complaint/add | Create a complaint | 
| GET | /complaint/get/{id} | Get complaint by ID | 
| GET | /complaint/get/date/{date} | Get complaints by date | 
| PATCH / PUT | /complaint/update/{id} | Update complaint | 
| DELETE | /complaint/delete/{id} | Delete complaint | 
| GET | /train_details/{train_no} | Get train info | 
| DELETE | /media/delete/{id} | Delete media | 


Explore all endpoints at:
http://localhost:8000/rs_microservice/docs


### 5. Testing

Use Postman or Swagger UI to test endpoints.
To test email delivery:

```bash
python test_email.py
```

### Author
Pragya Sharma
Github : @Pragyapssharma