# Vithy Project Setup

## Project Stack

Frontend:
- Flutter

Backend:
- Spring Boot

Database:
- PostgreSQL

---

# Prerequisites

Install:

Flutter SDK
Android Studio
Java 21
PostgreSQL 16
Git

Verify:

flutter doctor

java -version

psql --version

---

# Clone Repositories

Backend:

git clone https://github.com/KhornMolika/vithy-backend.git

Frontend:

git clone https://github.com/KhornMolika/vithy-frontend.git

---

# Backend Setup

Open backend:

cd vithy_backend

Install dependencies:

./mvnw clean install

Create database:

CREATE DATABASE vithy_db;

Configure:

src/main/resources/application.properties

Example:

spring.datasource.url=jdbc:postgresql://localhost:5432/vithy_db

spring.datasource.username=postgres

spring.datasource.password=your_password

Run backend:

./mvnw spring-boot:run

Backend URL:

http://localhost:8080

---

# Frontend Setup

Open frontend:

cd vithy_frontend

Install packages:

flutter pub get

Run application:

flutter run

---

# Environment Variables

Backend:

DB_URL=
DB_USERNAME=
DB_PASSWORD=

Frontend:

API_URL=http://localhost:8080

---

# Verify Installation

Backend:

http://localhost:8080

Frontend:

Application launches successfully

Database:

Connected successfully

Checklist:

[ ] Backend running

[ ] Frontend running

[ ] Database connected

[ ] API reachable

---

# Common Issues

Port already used:

Windows:

netstat -ano | findstr :8080

Flutter issues:

flutter clean

flutter pub get

Database issue:

Start PostgreSQL service

---

# Team Rules

Do not push directly to main.

Develop inside feature branches.

Merge through Pull Request.

Follow WORKFLOW.md.
