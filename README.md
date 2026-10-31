# GreenOps Sentinel

> AI-Driven Cloud Cost Optimization & Carbon Footprint Reduction using Spring Boot, AWS, Google Gemini, Docker, and PostgreSQL.

![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.x-brightgreen)
![AWS](https://img.shields.io/badge/AWS-EC2%20%7C%20CloudWatch-yellow)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📖 Overview

GreenOps Sentinel is an AI-powered cloud monitoring platform that automatically identifies underutilized AWS EC2 instances, analyzes infrastructure usage using Google Gemini AI, and generates intelligent recommendations to reduce cloud costs and carbon emissions.

Unlike traditional monitoring tools that rely on static thresholds, GreenOps Sentinel combines real-time AWS CloudWatch metrics with Generative AI to provide contextual FinOps recommendations.

---

## ✨ Features

- 🔍 Automatically discovers running EC2 instances
- 📊 Retrieves live CPU utilization from AWS CloudWatch
- 🤖 Uses Google Gemini AI for intelligent cloud optimization recommendations
- 💾 Stores audit history in PostgreSQL
- 🌐 RESTful API built with Spring Boot
- 🎨 Responsive Dark Mode Dashboard
- 🐳 Dockerized deployment
- ⚙️ GitHub Actions CI/CD Pipeline
- ❤️ Spring Boot Actuator Health Monitoring

---

# 🏗 Architecture

```
                +----------------------+
                |   Web Dashboard      |
                +----------+-----------+
                           |
                           |
                    REST API (Spring Boot)
                           |
        +------------------+------------------+
        |                                     |
        |                                     |
 AWS CloudWatch                      Google Gemini AI
        |                                     |
        +---------------+---------------------+
                        |
                 AI Recommendation
                        |
                 PostgreSQL Database
```

<img width="628" height="420" alt="Picture" src="https://github.com/user-attachments/assets/ebda4160-7ab6-4a37-8e4d-a8c7bac250ef" />


---

# 🛠 Tech Stack

## Backend

- Java 21+
- Spring Boot
- Spring Data JPA
- Spring AI

## Cloud

- AWS EC2
- AWS CloudWatch
- AWS SDK v2

## AI

- Google Gemini API

## Database

- PostgreSQL

## DevOps

- Docker
- Docker Compose
- GitHub Actions

## Frontend

- HTML5
- CSS3
- JavaScript

---

# 📂 Project Structure

```
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

# ⚙️ How It Works

1. Discover running EC2 instances.
2. Fetch CPU metrics from AWS CloudWatch.
3. Send metrics to Google Gemini AI.
4. Generate optimization recommendations.
5. Store audit results in PostgreSQL.
6. Display insights on the dashboard.

---

# 📡 API Endpoints

## Get All Audit Records

```
GET /api/audits
```

Response

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

---

## Health Check

```
GET /actuator/health
```

---

# 🐳 Docker

Start the application

```bash
docker-compose up --build
```

Stop containers

```bash
docker-compose down
```

---

# 🚀 Running Locally

### Clone Repository

```bash
git clone https://github.com/Mainuddeen00/GreenOps-Sentinel.git
```

```bash
cd GreenOps-Sentinel
```

### Configure Environment Variables

```
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=

SPRING_AI_GOOGLE_API_KEY=

POSTGRES_DB=
POSTGRES_USER=
POSTGRES_PASSWORD=
```

### Run PostgreSQL

```bash
docker-compose up postgres
```

### Run Spring Boot

```bash
./mvnw spring-boot:run
```

---

# 📊 Workflow

```
Running EC2 Instance
          │
          ▼
 AWS CloudWatch Metrics
          │
          ▼
 Spring Boot Service
          │
          ▼
 Google Gemini AI
          │
          ▼
 AI Recommendation
          │
          ▼
 PostgreSQL
          │
          ▼
 REST API
          │
          ▼
 Web Dashboard
```

---

# 💡 Future Improvements

- Automated EC2 shutdown using AWS Lambda
- Multi-cloud support (Azure & GCP)
- Memory, Disk, and Network monitoring
- Carbon footprint calculator
- Scheduled hourly audits
- Email & Slack notifications
- Predictive cloud cost analytics

---

# 📸 Screenshots

Add screenshots here.

```
screenshots/
    dashboard.png
    cloudwatch.png
    github-actions.png
    docker.png
```

---

# 📈 CI/CD

The project uses GitHub Actions to:

- Build the project
- Run Maven package
- Validate code
- Build Docker image

Automatically triggered on every push to the `main` branch.

---

# 🌍 Real World Applications

- Enterprise Cloud Cost Optimization
- FinOps Automation
- Green Computing
- Sustainable Cloud Infrastructure
- AI-powered Infrastructure Monitoring

---

# 👨‍💻 Author

**Mainuddeen**

B.Tech Computer Science & Engineering  
Lovely Professional University

- GitHub: https://github.com/Mainuddeen00
- LinkedIn: https://www.linkedin.com/in/mainuddeen0/

---

# ⭐ If you found this project useful

Give this repository a ⭐ and feel free to contribute!
