<div align="center">

# TUNGO

### Multi-Platform Intercity Transportation System

A digital platform for managing intercity shared transportation, connecting passengers, drivers, supervisors, stations and administrators through mobile applications, web dashboards and a centralized backend.

**Final-Year Engineering Project — ESPRIT**

</div>

---

## Overview

**TUNGO** is a multi-platform transportation system designed to digitize intercity shared-transport workflows in Tunisia.

The platform brings together passenger services, driver operations and administrative management in one system.

It includes:

- a passenger mobile application;
- a driver mobile application;
- web dashboards for operational management;
- a centralized REST API;
- authentication and role-based access;
- reservation and trip management;
- parcel management;
- routes, schedules, stations and cities;
- real-time application features;
- an AI-assisted chatbot.

---

## System Architecture

```text
                    ┌─────────────────────┐
                    │   Passenger App     │
                    │      Flutter        │
                    └──────────┬──────────┘
                               │
                               │
                    ┌──────────▼──────────┐
                    │                     │
                    │    Backend API      │
                    │  Node.js / Express  │
                    │                     │
                    │ Authentication      │
                    │ Reservations        │
                    │ Routes & Schedules  │
                    │ Parcels             │
                    │ Users & Roles       │
                    │ AI Assistant        │
                    │                     │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼

     ┌──────────────┐   ┌──────────────┐   ┌─────────────────┐
     │  Driver App  │   │ PostgreSQL   │   │ Web Dashboards  │
     │   Flutter    │   │   Database   │   │      React      │
     └──────────────┘   └──────────────┘   └─────────────────┘
```

---

## Repository Organization

The project is organized across several branches:

| Branch | Component |
|---|---|
| `main` | Project overview |
| `backend` | Backend API and business logic |
| `client-mobile-app` | Passenger Flutter application |
| `chauffeur-mobile-app` | Driver Flutter application |
| `dashboards-web` | Web dashboards |

This structure keeps the main components of the platform separated while maintaining them inside the same project repository.

---

## Passenger Mobile Application

The passenger application provides the customer-facing side of TUNGO.

Built with **Flutter**, it allows passengers to interact with transportation services from a mobile device.

### Main Features

- User registration and authentication
- Search available transportation routes
- View schedules
- Make reservations
- Manage bookings
- Access trip information
- Manage parcel-related services
- View account information
- Interact with platform services

---

## Driver Mobile Application

The driver application supports operational workflows for drivers.

Also built with **Flutter**, it provides access to information related to assigned transportation activities.

### Main Features

- Driver authentication
- Access assigned trips
- View schedules and routes
- Manage trip-related information
- Interact with passenger and operational data
- Access transportation workflow information

---

## Web Dashboards

The web component provides management interfaces for platform operations.

The dashboards support several administrative roles and allow authorized users to manage the transportation system from a browser.

### Managed Data

- Users
- Drivers
- Stations
- Cities
- Routes
- Schedules
- Reservations
- Parcels
- Transportation operations

---

## Backend

The backend provides the central API used by the mobile applications and web dashboards.

### Main Responsibilities

- Authentication
- Authorization
- User management
- Reservation management
- Route management
- Schedule management
- Station and city management
- Parcel workflows
- Driver-related operations
- Data persistence
- API communication with the different clients

---

## Authentication & Authorization

The platform uses token-based authentication to protect its APIs.

```text
User Login
    │
    ▼
Credentials Validation
    │
    ▼
JWT Token
    │
    ▼
Authenticated Request
    │
    ▼
Protected API
```

Different platform roles have access to different functionality.

---

## Reservation Flow

A simplified reservation workflow:

```text
Passenger
    │
    ▼
Select Route
    │
    ▼
Select Schedule
    │
    ▼
Create Reservation
    │
    ▼
Backend Validation
    │
    ▼
Store Reservation
    │
    ▼
Reservation Available
to Platform Users
```

---

## Transportation Data

The system manages the relationships between:

```text
Cities
  │
  ▼
Stations
  │
  ▼
Routes
  │
  ▼
Schedules
  │
  ▼
Trips / Reservations
```

This structure provides the foundation for the platform's transportation workflows.

---

## Parcel Management

TUNGO also includes workflows related to parcel transportation.

The platform can manage parcel information alongside passenger transportation operations.

This functionality extends the system beyond passenger reservations and supports additional intercity transport use cases.

---

## AI Assistant

The backend includes AI-related configuration for an assistant integrated with the platform.

The assistant is intended to help users obtain contextual information through the application.

The backend configuration includes external AI service integration and model-related environment variables.

---

## Tech Stack

### Mobile

<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/flutter/flutter-original.svg" width="44" height="44" alt="Flutter" />
  &nbsp;&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/dart/dart-original.svg" width="44" height="44" alt="Dart" />
</p>

**Flutter · Dart**

---

### Web

<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" width="44" height="44" alt="React" />
  &nbsp;&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" width="44" height="44" alt="JavaScript" />
</p>

**React · JavaScript**

---

### Backend

<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg" width="44" height="44" alt="Node.js" />
  &nbsp;&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/express/express-original.svg" width="44" height="44" alt="Express" />
</p>

**Node.js · Express.js · REST APIs · JWT**

---

### Database

<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg" width="44" height="44" alt="PostgreSQL" />
</p>

**PostgreSQL**

---

### DevOps & Tools

<p>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg" width="44" height="44" alt="Docker" />
  &nbsp;&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jenkins/jenkins-original.svg" width="44" height="44" alt="Jenkins" />
  &nbsp;&nbsp;
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" width="44" height="44" alt="Git" />
</p>

**Git · Docker · Jenkins · CI/CD**

---

## Backend Setup

Switch to the backend branch:

```bash
git checkout backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file containing the required configuration.

The backend currently uses variables including:

```env
PORT=

DB_NAME=
DB_USER=
DB_PASSWORD=
DB_HOST=
DB_PORT=
DATABASE_URL=

JWT_SECRET_KEY=

ADMIN_EMAIL=
ADMIN_PASSWORD=

HF_TOKEN=
GOOGLE_API_KEY=
GOOGLE_MODEL=

EMAIL_USERNAME=
EMAIL_PASSWORD=
```

Do not commit real credentials or API keys to Git.

---

## Run the Backend

Development mode:

```bash
npm run dev
```

Or:

```bash
npm start
```

The main server starts from:

```text
server.js
```

---

## Passenger App Setup

Switch to:

```bash
git checkout client-mobile-app
```

Install Flutter dependencies:

```bash
flutter pub get
```

Run the application:

```bash
flutter run
```

---

## Driver App Setup

Switch to:

```bash
git checkout chauffeur-mobile-app
```

Install dependencies:

```bash
flutter pub get
```

Run:

```bash
flutter run
```

---

## Web Dashboard Setup

Switch to:

```bash
git checkout dashboards-web
```

Install the project dependencies according to the web application configuration and start the development environment.

---

## Engineering Areas

TUNGO combines several software engineering areas in one project:

- Full-stack development
- Cross-platform mobile development
- REST API design
- Authentication and authorization
- Relational data modeling
- Multi-role applications
- Transportation workflows
- Real-time application features
- AI integration
- CI/CD
- Multi-client architecture

---

## Academic Context

TUNGO was developed as a **Final-Year Engineering Project at ESPRIT**.

The project focused on designing a complete software ecosystem composed of mobile applications, web interfaces and backend services around a common transportation domain.

---

## Project Status

TUNGO is an academic engineering project.

The repository contains the different components required to demonstrate the system architecture and its main workflows.

Environment configuration, credentials and external service keys must be configured separately before running the complete platform.

---

## Author

**Iheb Jdey**

Software Engineer · Full-Stack · Mobile · Applied AI

[Portfolio](https://ihebjdey.tn) ·
[LinkedIn](https://www.linkedin.com/in/jdey-iheb) ·
[GitHub](https://github.com/ihebjdey2)
