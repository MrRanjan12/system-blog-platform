# Blog System

A full-stack application built to explore how a structured content system behaves — from request handling and data flow to authentication and state management.

---

## Overview

This project focuses on building a backend-driven blog system with clear separation of concerns, predictable data flow, and controlled access through authentication.

Rather than treating it as a feature-based application, the goal was to understand how individual components interact under typical usage patterns — including CRUD operations, user isolation, and request validation.

---

## Architecture

Frontend and backend are maintained as separate layers:

- Frontend handles routing, state, and API interaction  
- Backend manages data persistence, authentication, and business logic
- 
/frontend → React application
/backend → Express API layer

---

## Backend Structure

/models
├── Blog.js
└── User.js

/controllers
├── blogController.js
└── authController.js

/routes
├── blogRoutes.js
└── authRoutes.js

/middleware
└── authMiddleware.js

index.js
.env


The backend is organized around responsibility:
- Models define structure  
- Controllers handle logic  
- Routes define access points  
- Middleware enforces constraints (authentication)  

---

## Core Capabilities

- Controlled blog creation, update, and deletion  
- User authentication using token-based flow  
- Isolation of user-specific data  
- Structured API design with predictable endpoints  

---

## API Design

### Auth

- POST /auth/register  
- POST /auth/login  

### Posts

- GET /posts  
- GET /posts/:id  
- POST /posts (protected)  
- PUT /posts/:id (protected)  
- DELETE /posts/:id (protected)  

---
## Technology

- Frontend: React, Axios, Tailwind  
- Backend: Node.js, Express  
- Database: MongoDB (Mongoose)  
- Auth: JWT  

---

## Implementation Notes

- Passwords are hashed before storage  
- Authentication is enforced via middleware  
- Tokens are passed through request headers  
- Token persistence uses local storage (can be improved using httpOnly cookies)  

---

## Setup


git clone https://github.com/MrRanjan12/BlogWebsite.git

cd BlogWebsite 
git clone https://github.com/MrRanjan12/BlogWebsite.git

cd BlogWebsite


### Backend


cd backend
npm install
npm start


### Frontend


cd frontend
npm install
npm run dev


---

## Direction

This project is part of a broader focus on understanding backend systems, API design, and how state and data flow are managed across layers.

Further iterations will focus on improving structure, handling edge cases, and extending the system with more complex interactions.
