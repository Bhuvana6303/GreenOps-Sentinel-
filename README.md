# GreenOps Sentinel

> AI-Driven Cloud Cost Optimization & Carbon Footprint Reduction using Spring Boot, AWS, Google Gemini, Docker, and PostgreSQL.

**Developed by Bhuvana Gundepalli**

![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.x-brightgreen)
![AWS](https://img.shields.io/badge/AWS-EC2%20%7C%20CloudWatch-yellow)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📖 Overview

GreenOps Sentinel is an AI-powered cloud monitoring platform that automatically identifies underutilized AWS EC2 instances, analyzes infrastructure usage using Google Gemini AI, and generates intelligent recommendations to reduce cloud costs and carbon emissions.

Unlike traditional monitoring tools that rely on static thresholds, GreenOps Sentinel combines AWS CloudWatch metrics with Generative AI to provide contextual FinOps recommendations.

## ✨ Features

- 🔍 Automatically discovers running AWS EC2 instances.
- 📊 Retrieves CPU utilization metrics from AWS CloudWatch.
- 🤖 Uses Google Gemini AI for intelligent cloud optimization recommendations.
- 💾 Stores audit history in PostgreSQL.
- 🌐 RESTful API built with Spring Boot.
- 🎨 Responsive Dark Mode Dashboard.
- 🐳 Dockerized deployment.
- ⚙️ GitHub Actions CI/CD Pipeline.
- ❤️ Spring Boot Actuator Health Monitoring.

---

## 🏗 Architecture

```text
                +----------------------+
                |   Web Dashboard      |
                +----------+-----------+
                           |
                    REST API
                    Spring Boot
                           |
          +----------------+----------------+
          |                                 |
          |                                 |
    AWS CloudWatch                   Google Gemini AI
          |                                 |
          +----------------+----------------+
                           |
                   AI Recommendation
                           |
                  PostgreSQL Database
```

## 🛠 Tech Stack

### Backend
- Java 21+
- Spring Boot
- Spring Data JPA
- Spring AI

### Cloud
- AWS EC2
- AWS CloudWatch
- AWS SDK v2

### Artificial Intelligence
- Google Gemini API

### Database
- PostgreSQL

### DevOps
- Docker
- Docker Compose
- GitHub Actions

### Frontend
- HTML5
- CSS3
- JavaScript

---

## 📂 Project Structure

```text
GreenOps-Sentinel/
│
├── backend/
│   ├── controller/
│   ├── service/
│   ├── repository/
│   ├── model/
│   └── config/
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── docker-compose.yml
├── Dockerfile
├── pom.xml
└── README.md
```

---

## ⚙️ How It Works

1. Discovers running AWS EC2 instances.
2. Fetches CPU utilization metrics from AWS CloudWatch.
3. Sends infrastructure metrics to Google Gemini AI.
4. Generates intelligent cloud optimization recommendations.
5. Stores audit results in PostgreSQL.
6. Displays optimization insights on the dashboard.

---

## 📡 API Endpoints

### 1. Get All Audit Records

**Endpoint:**

```http
GET /api/audits
```

**Example Response:**

```json
[
  {
    "instanceId": "i-xxxxxxxxxxxx",
    "cpuUsage": 2.54,
    "aiRecommendation": "Consider stopping this instance.",
    "auditTime": "2026-05-20T12:30:21"
  }
]
```

### 2. Health Check

**Endpoint:**

```http
GET /actuator/health
```

---

## 🐳 Docker

### Start the Application

```bash
docker-compose up --build
```

### Stop Containers

```bash
docker-compose down
```

---

## 🚀 Running Locally

### Step 1: Clone the Repository

```bash
git clone https://github.com/Bhuvana6303/GreenOps-Sentinel-.git
```

### Step 2: Navigate to the Project Directory

```bash
cd GreenOps-Sentinel-
```

### Step 3: Configure Environment Variables

Create a `.env` file in the project directory and configure the following:

```env
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=

SPRING_AI_GOOGLE_API_KEY=

POSTGRES_DB=
POSTGRES_USER=
POSTGRES_PASSWORD=
```

**Important:** Never upload your actual AWS credentials, Gemini API key, database passwords, or `.env` file to GitHub.

### Step 4: Build and Run Using Docker

```bash
docker-compose up --build
```

---

## 🔐 Security

- Keep AWS credentials private.
- Use environment variables for sensitive configurations.
- Never commit API keys or database passwords.
- Follow AWS IAM least-privilege principles.

---

## 👩‍💻 Author

**Bhuvana Gundepalli**

🎓 B.Tech – Computer Science and Engineering

- **GitHub:** [Bhuvana6303](https://github.com/Bhuvana6303)
- **LinkedIn:** [Bhuvana Gundepalli](https://www.linkedin.com/in/bhuvanagundepalli/)

---

## 🎯 Project Information

| Category | Details |
|---|---|
| Project Name | GreenOps Sentinel |
| Domain | Cloud Computing |
| Subdomain | FinOps and GreenOps |
| AI Technology | Google Gemini |
| Backend | Java, Spring Boot |
| Cloud Platform | AWS |
| Database | PostgreSQL |
| Containerization | Docker |

---

⭐ If you find this project interesting, feel free to explore the repository!

**GreenOps Sentinel – Smarter Cloud Optimization for a Sustainable Future.**
