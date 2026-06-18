# Academic Performance Early-Warning System (APEWS)

[cite_start]An intelligent, analytical web-based application designed for higher education institutions to shift academic performance management from a reactive approach to a proactive, preventive model[cite: 33, 56]. [cite_start]APEWS regularly monitors key student indicators (attendance, test results, and workload), runs a rule-based risk classification engine, and alerts stakeholders to facilitate timely academic intervention[cite: 27, 28, 52].

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [System Architecture & Design (SDA)](#-system-architecture--design-sda)
  - [Domain Model & Structural Design](#domain-model--structural-design)
  - [Behavioral & Data Flow Modeling](#behavioral--data-flow-modeling)
- [System Requirements](#-system-requirements)
  - [Functional Requirements](#functional-requirements)
  - [Non-Functional Requirements](#non-functional-requirements)
- [User Roles & Stakeholders](#-user-roles--stakeholders)
- [Tech Stack & Deployment](#-tech-stack--deployment)
- [Team Members](#-team-members)

---

## 🚀 Project Overview

[cite_start]In traditional educational settings, student academic deterioration is often detected too late—usually after a significant decline like repeated failures or low attendance has already occurred[cite: 23]. 

[cite_start]**APEWS** serves as a supplementary analytical layer that integrates with existing Student Information Systems (SIS) and Learning Management Systems (LMS)[cite: 35, 60]. [cite_start]It parses available data every 24 hours to classify students into **Low, Medium, or High risk levels**, allowing academic advisors to step in before irreversible academic decline takes place[cite: 44, 45, 114].

---

## ✨ Key Features

- [cite_start]**Automated Academic Monitoring:** Continuously syncs attendance records, assignment completions, quizzes, and exam scores[cite: 51, 106].
- [cite_start]**Risk Classification Engine:** Computes a weighted risk score using standard or custom-configured threshold parameters[cite: 52, 116].
- [cite_start]**Real-Time Dashboards:** Tailored role-appropriate interfaces displaying risk trends (improving/stable/declining) for students, faculty, and advisors[cite: 108, 117].
- [cite_start]**Automated Alerts:** Triggers instant email and in-system push notifications within 24 hours of any student risk escalation[cite: 109, 118].
- [cite_start]**Intervention Logging:** A secure portal for academic advisors to schedule meetings, record support plans, log outcomes, and monitor history[cite: 76, 110].
- [cite_start]**Reporting & Analytics:** Generates programmatic monthly or on-demand distribution and effectiveness metrics for department administrators[cite: 111, 123].

---

## 🏗 System Architecture & Design (SDA)

[cite_start]This project has been developed strictly adhering to standard object-oriented analysis and software design patterns[cite: 13]. 

### Domain Model & Structural Design
[cite_start]The core business logic is engineered around loosely coupled software modules to ensure high maintainability and ease of horizontal scaling[cite: 140, 141]. 
- **Class Diagrams:** Embody encapsulated entities for `User`, `Student`, `Advisor`, `AcademicRecord`, `RiskStatus`, and `InterventionLog`.
- [cite_start]**Package Architecture:** Segregated into Presentation (UI/Dashboards), Business Logic (Risk Classification Engine), Integration (SIS/LMS API Connectors), and Data Access layers[cite: 58, 124].

### Behavioral & Data Flow Modeling
[cite_start]The dynamic aspects of the system are detailed through extensive UML behavioral diagrams[cite: 14]:
- [cite_start]**Use Case Diagrams:** Define boundary interactions across all four primary human actors and external sub-systems[cite: 144].
- [cite_start]**System Sequence Diagrams (SSD):** Map exact system input/output event loops for critical workflows such as `Risk Assessment`, `Alert Notification`, and `Intervention Logging`[cite: 244, 246, 250].
- **Data Flow Diagram (DFD Level 0):** Illustrates the macro data streaming flow from the SIS/LMS through the classification engine out to the notification delivery networks and advisor dashboards.

---

## 📋 System Requirements

### Functional Requirements (Core Subset)
| ID | Requirement Description |
| :--- | :--- |
| **FR-01** | [cite_start]Synchronize academic data from institutional systems at intervals $\le$ 24 hours[cite: 114]. |
| **FR-02** | [cite_start]Compute risk using weighted metrics: Attendance (30%), Assignments (20%), Quizzes (20%), Exams (30%)[cite: 115]. |
| **FR-03** | [cite_start]Classify students into Low, Medium, or High risk tiers based on runtime configuration values[cite: 116]. |
| **FR-05** | [cite_start]Dispatch automated escalation notifications to both student and assigned advisor within 24 hours of tier changes[cite: 118]. |
| **FR-08** | [cite_start]Allow administrators to re-adjust weight weightings and risk boundaries dynamically without redeploying the application[cite: 121]. |
| **FR-09** | [cite_start]Enforce an immutable cryptographic audit log tracking all user data access events[cite: 122]. |

### Non-Functional Requirements
- [cite_start]**Performance (NFR-01):** Dashboard render time $< 3$ seconds for up to 200 concurrent user threads[cite: 133].
- [cite_start]**Security (NFR-03):** Role-Based Access Control (RBAC) integrated with institutional Single Sign-On (SSO); data encrypted using TLS 1.2+ in transit[cite: 135, 136].
- [cite_start]**Scalability (NFR-04):** Read-heavy database tuning to scale horizontally up to 20,000 active student records[cite: 137].
- [cite_start]**Availability (NFR-02):** Minimum target uptime of 99.5% throughout the active academic semesters[cite: 134].

---

## 👥 User Roles & Stakeholders

1. [cite_start]**Students:** Access a private portal to view personal performance indicators and act on personalized improvement paths[cite: 85, 120].
2. [cite_start]**Academic Advisors:** Monitor assigned students daily, manage alerts, and log targeted interventions[cite: 75, 76].
3. [cite_start]**Faculty Members:** Confirm attendance baselines and review risk indicators for students enrolled in their active courses[cite: 81, 84].
4. [cite_start]**Department Administrators:** Manage strategic parameter thresholds, oversee broad program trends, and access macro-analytical reports[cite: 89, 90].

---

## 💻 Tech Stack & Deployment

- **Architecture Style:** Layered Architecture / MVC (Model-View-Controller) pattern.
- [cite_start]**Frontend:** Fully responsive web design accommodating displays from 375px up to 1920px (HTML5, CSS3, JavaScript Frameworks)[cite: 139].
- [cite_start]**Integration Layer:** RESTful APIs & CSV parser engines for seamless legacy system handshakes[cite: 124].
- [cite_start]**Deployment Platform:** Tailored for cloud environments (AWS / Azure) or localized on-premises Linux infrastructure using containerization[cite: 141].

---

## ✒️ Team Members

[cite_start]Developed by the Department of Computer Sciences at **FAST - National University of Computer & Emerging Sciences**, Chiniot-Faisalabad Campus[cite: 315, 316, 317]:

- [cite_start]**Shaiza Hamid** (24F-0585) [cite: 313]
- [cite_start]**Ayesha Naeem** (24F-0586) [cite: 314]

[cite_start]*Prepared in March 2026 as part of the BS Course Project.* [cite: 318, 337]
