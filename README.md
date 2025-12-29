# backend-CareSync
# CareSync — Backend

CareSync Backend is a RESTful API powering the CareSync wellness tracking Progressive Web Application (PWA).

It handles authentication, daily well-being check-ins, wellness score computation, analytics preparation, and strict data privacy enforcement.

>  CareSync is **not a medical system**.  
> It is a self-observation and prevention tool designed to improve awareness and understanding of personal well-being patterns.

---

##  Responsibilities

The backend is responsible for:

- Secure user authentication and authorization (JWT)
- Daily check-in management (mood, energy, stress, sleep)
- Wellness score computation
- Analytics-ready data exposure
- Business rules and validation
- GDPR-compliant data handling (export & deletion)
- Stable REST API for a frontend PWA

---

##  Architecture

CareSync backend follows a **MVC + N-Tier architecture** to ensure scalability and maintainability.

### Layers

- **Controller Layer**
  - REST endpoints
  - Request/response handling
  - Input validation

- **Service Layer**
  - Business logic
  - Wellness score computation
  - Rule enforcement
  - Framework-independent logic where possible

- **Data Access Layer**
  - JPA repositories
  - Entity persistence
  - DTO mapping

- **Database Layer**
  - Relational database
  - Historical data storage for trend analysis

---

## Core Domain Concepts

### User
Authenticated application user.

### Daily Check-in
A daily record containing:
- Mood
- Energy level
- Stress level
- Sleep quality
- Optional note
- Timestamp

### Wellness Score
A synthetic daily indicator representing the user's overall well-being.

### Insights (MVP 3)
Explainable signals derived from cumulative data:
- Progressive fatigue
- Sustained stress
- Energy decline patterns

---

##  Security

- JWT-based authentication
- Password hashing
- User-level data isolation
- Centralized exception handling
- Input validation

---

##  Analytics & Data Processing

From MVP 2 onward:
- Clean dataset preparation
- Trend and average computation
- Python-based analytics integration
- Correlation and weak signal detection

---

##  Testing & Quality

- Unit tests on business logic
- Wellness score validation
- Insight rule testing
- Emphasis on readability and maintainability

---

##  MVP Roadmap

- **MVP 1**: Authentication, daily check-ins, wellness score
- **MVP 2**: Trends and analytics
- **MVP 3**: Insight engine

---

## Tech Stack

- Java 21
- Spring Boot
- Spring Security (JWT)
- Spring Data JPA
- Bean Validation
- PostgreSQL
- Maven

---

##  Author

**Hapssatou Sy**  
Software Engineer — Full Stack & Data  
Project: CareSync
