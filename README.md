# FootballStats

**Project to view the statistics of the world's major leagues.**

## 🌍 Overview

**FootballStats** is a full-stack web application designed to display comprehensive statistics from the world's top football leagues. The project follows a **microservices architecture**, integrating multiple technologies to simulate a production-grade system with a strong backend, efficient frontend, and real-time data scraping.

## ⚙️ Architecture

- **Backend**:
    - **Python**: used for web scraping football data from public sources.
    - **Java + Spring Boot**: handles business logic, REST APIs, and microservice orchestration.
- **Frontend**:
    - **Angular** (TypeScript): interactive, responsive Single Page Application (SPA).
- **Database**:
    - **PostgreSQL**: relational database to store structured football data.
- **Architecture Pattern**:
    - **Microservices** with Docker and REST APIs for communication between services.

### 🧩 Architecture Diagram

+---------------------+ REST +--------------------------+
| Angular Frontend | <-------------- | API Gateway (Spring) |
+---------------------+ +--------------------------+
|
┌───────────────────────────────────────┴─────────────────────────────┐
| | |
+-------------------+ +------------------------+ +-------------------------+
| Team Service | | Player Service | | Match Service |
| (Spring Boot) | | (Spring Boot) | | (Spring Boot) |
+-------------------+ +------------------------+ +-------------------------+
| | |
└───────────────┬──────────────┴──────────────┬───────────────────────┘
| |
+------------------+ +---------------------------+
| PostgreSQL DB | | Python Scraper Service |
| (Football Data) | | (Scheduled or On-Demand) |
+------------------+ +---------------------------+

## 📌 Features

- Real-time scraping and ingestion of football data
- RESTful APIs for accessing leagues, teams, players, and match stats
- Angular frontend with interactive components and filtering
- PostgreSQL persistence with optimized queries and relationships
- Dockerized setup for local development and deployment

## 🏆 Supported Leagues

- Premier League
- La Liga
- Bundesliga
- Serie A
- Ligue 1
- Major League Soccer
- (Others planned)

## 🚀 Getting Started

### Prerequisites

- Java 21+
- Python 3.12.3+
- Typescript 18+
- PostgreSQL 14+
- Docker & Docker Compose
- Kubernetes
- Kafka

---

### 🧱 Project Structure

footballstats/
├── backend/
│ ├── scraper/ # Python scraper service
│ └── spring-services/ # Java microservices
├── frontend/ # Angular app
├── database/ # SQL scripts / docker configs
├── docker-compose.yml
└── README.md

---

### 🛠️ Tech Stack

- **Python** – Scraping (BeautifulSoup, Requests)
- **Java + Spring Boot** – REST APIs, microservices
- **Angular + TypeScript** – Frontend SPA
- **PostgreSQL** – Relational data storage
- **Docker** – Containerization of services
- **Swagger / OpenAPI** – API documentation
- **GitHub Actions** *(futuro)* – CI/CD pipelines

---

### 📈 Roadmap

- [x] Web scraping service funcional
- [ ] Microservicios Spring Boot iniciales
- [ ] Conexión con PostgreSQL
- [ ] Autenticación y gestión de usuarios
- [ ] Favoritos y seguimiento de equipos/jugadores
- [ ] Integración de modelo ML para predicciones
- [ ] Despliegue en Kubernetes (etapa avanzada)

---

### 📦 Clone the Repository

```bash
git clone https://github.com/tuusuario/footballstats.git
cd footballstats
```

---

## 🙌 Contributing

Pull requests are welcome! Please fork the repository and open an issue to discuss improvements or bugs before submitting changes.

---

## 👨‍💻 Author

\[Marcos López Marín] - Software Engineer passionate about AI, NLP, and career tech.

---

## 📄 License

This project is licensed under the MIT License.
