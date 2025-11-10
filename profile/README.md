# 🏗️ DEVision – Squad Hercules (EEET2582 / ISYS3461)

> “An Cư Lạc Nghiệp” – *Settled and Flourished*  
> A microservice-based job recruitment ecosystem connecting job seekers and employers in the Computer Science field.

---

## 🌍 Project Overview

**DEVision** is a two-subsystem platform that bridges **Job Applicants** and **Job Managers** in a transparent, secure, and scalable way.

- **Job Applicant Subsystem**: Enables users to register, manage profiles, search and apply for jobs, and subscribe for real-time notifications.
- **Job Manager Subsystem**: Allows companies to create job posts, manage applications, search for applicants, and receive notifications for matching candidates.

The system follows a **microservice architecture** using **Spring Boot** for the backend, a **componentized React** frontend, and asynchronous communication through **Kafka**.  
All services are **containerized with Docker** and can be **orchestrated using Kubernetes** for scalability and resilience.

---

## 👥 Squad Hercules – Team Members & Roles

### 🔹 Overall Squad Role Distribution

| Role                                | Count | Responsibility                                                                                                          | Members                                               |
| ----------------------------------- | ----- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| **Product Owner (PO)**              | 1     | Oversees vision, coordinates both subteams, ensures feature alignment between Applicant ↔ Manager. Reports to lecturer. | **Le Trung Kien** *(also PM of JA)*                   |
| **Project Manager / Scrum Master**  | 1     | Facilitates standups, sprint tracking, and resolves blockers for both subteams. Maintains GitHub Project board.         | **Ho Quang Huy** *(also PM of JM)*                    |
| **Backend Lead (Microservices)**    | 2     | Define service boundaries, integration via REST + Kafka, manage data models, ensure deployment consistency.             | **Nguyen Hoang Son (JA)**, **Nguyen Trong Khoa (JM)** |
| **Frontend Lead (React)**           | 2     | Define component hierarchy, enforce reusable UI pattern, REST helper, code review for UI PRs.                           | **Ung Xuan Dat (JA)**, **Nguyen Hong Anh (JM)**       |
| **DevOps & Integration Engineer**   | 2     | Docker/Kafka/Redis setup, CI/CD, API Gateway, Kubernetes orchestration.                                                 | **Nguyen Tan Phat (JA)**, **Vu Thien Minh Hao (JM)**  |
| **Full Stack / Feature Integrator** | 2     | Bridge frontend-backend for features like Job Post ↔ Application, Subscription flow, testing APIs.                      | **Chau Tung Nguyen (JA)**, **Duong Phu Dong (JM)**    |

---

### 🔸 Job Applicant Subteam (Subsystem A)

| Member               | Primary Role                | Key Responsibilities                                                                     |
| -------------------- | --------------------------- | ---------------------------------------------------------------------------------------- |
| **Le Trung Kien**    | Product Owner & Coordinator | Overall system vision, ensure both subsystems integrate correctly, final documentation.  |
| **Nguyen Hoang Son** | Backend Lead                | Architect & implement microservices (Auth, Profile, Application). Manage MongoDB shards. |
| **Ung Xuan Dat**     | Frontend Lead               | Create reusable React components, REST helper, manage routing and design consistency.    |
| **Chau Tung Nguyen** | Full Stack Integrator       | Connect API calls to backend services, test end-to-end flow, fix integration bugs.       |
| **Nguyen Tan Phat**  | DevOps / Infrastructure     | Docker Compose setup for JA, Redis, Kafka producer, CI/CD scripts.                       |

---

### 🔸 Job Manager Subteam (Subsystem B)

| Member                | Primary Role          | Key Responsibilities                                                               |
| --------------------- | --------------------- | ---------------------------------------------------------------------------------- |
| **Ho Quang Huy**      | Scrum Master / PM     | Manage sprints, handle review meetings, ensure timely GitHub updates.              |
| **Nguyen Trong Khoa** | Backend Lead          | Implement microservices (Company, JobPost, Payment, Notification). Kafka consumer. |
| **Nguyen Hong Anh**   | Frontend Lead         | React UI components for company dashboard, job post management.                    |
| **Vu Thien Minh Hao** | DevOps Engineer       | Docker + Kafka orchestration for JM, networking with JA, CI/CD integration.        |
| **Duong Phu Dong**    | Full Stack Integrator | Integrate JM APIs with JA, handle API Gateway routes, perform feature testing.     |

---

### 🧭 Coordination Summary

- **Cross-team integration** handled by the **Backend Leads** (Son & Khoa) and **DevOps Engineers** (Phat & Hao).  
- **Frontend Leads** ensure design and component consistency between subsystems.  
- **Full Stack Integrators** verify functional flow across Applicant ↔ Manager subsystems.  
- **PO & PM** oversee progress, GitHub board updates, and lecturer communication.

---

## 🧩 System Architecture

| Layer | Technology | Description |
|--------|-------------|-------------|
| **Frontend** | React (Componentized Architecture) | Modular, reusable UI components with centralized REST HTTP helper. |
| **Backend** | Spring Boot Microservices | Independent services for authentication, profile, jobs, applications, and subscriptions. |
| **Communication** | Kafka + REST APIs | Event-driven messaging between subsystems and async notifications. |
| **Database** | MongoDB + Redis | Distributed data storage with caching and sharding support. |
| **Deployment** | Docker + Kubernetes (optional) | Containerized and scalable infrastructure. |

---

## 🚀 Repositories

| Repository | Description |
|-------------|-------------|
| [`JobApplicant`](https://github.com/ISYS3461-2025C-Hercules-DEVision/JobApplicant) | Job Applicant subsystem – frontend & backend microservices. |
| [`JobManager`](https://github.com/ISYS3461-2025C-Hercules-DEVision/JobManager) | Job Manager subsystem – frontend & backend microservices. |
| [`Integration`](https://github.com/ISYS3461-2025C-Hercules-DEVision/Integration) *(optional)* | Shared Kafka topics, API gateway configs, Docker orchestration. |
| [`Docs`](https://github.com/ISYS3461-2025C-Hercules-DEVision/Docs) | Reports, diagrams, project charters, and presentation materials. |

---

## 📅 Sprint Timeline

| Sprint | Duration | Key Deliverables |
|--------|-----------|------------------|
| **Sprint 1** | Nov 3 – Nov 17, 2025 | Repo setup, ER model, architecture draft, GitHub board. |
| **Sprint 2** | Nov 18 – Dec 1, 2025 | Auth & Login microservices, frontend routing, Milestone 1 report. |
| **Sprint 3** | Dec 2 – Dec 16, 2025 | Profile & Job APIs, Redis & Kafka configuration, integration tests. |
| **Sprint 4** | Dec 17 – Dec 31, 2025 | Premium subscription & notification, UI polish, testing. |
| **Sprint 5** | Jan 1 – Jan 13, 2026 | Full subsystem integration, Docker deployment, Milestone 2 presentation. |

---

## 📊 Project Management & Workflow

**Methodology:** SCRUM (2-week sprints)  
**Tracking Tool:** GitHub Projects (Kanban Board)

### 🧭 Board Columns
> Product Backlog → Sprint Backlog → In Progress → Review → Staging → Done

### 🧱 Branching Strategy
- `main`: stable milestone versions  
- `dev`: latest integrated development branch  
- `feature/*`: feature-specific branches  
- All merges into `main` require **peer review + successful CI build**

---

## 🧠 Communication Rules

- **Meetings:** Every 2–3 days via Microsoft Teams / Discord  
- **Daily Updates:** Shared on GitHub Discussions or Messenger  
- **Response Time:** Within 24 hours on weekdays, 48 hours on weekends  
- **Documentation:** Updated after each sprint (C4 diagrams, ER models, API references)

---

## 🔐 Quality and Security

- **Authentication:** JSON Web Encryption (JWE) tokens  
- **Data Protection:** Encrypted credentials and sensitive data  
- **Code Review:** Every PR must be peer-reviewed before merging  
- **Testing:** Unit + integration testing for all microservices

---

## 👨‍🏫 Lecturer Access

**Lecturer:** *Tri Huynh*  
Added as a collaborator to all repositories and GitHub Project Board for real-time monitoring and feedback.

---

## 🏁 Vision Statement

DEVision aims to embody Vietnam’s value of *“An Cư Lạc Nghiệp”* — helping people find meaningful careers by connecting skilled applicants and innovative employers through a modern, microservice-driven recruitment ecosystem.

---
