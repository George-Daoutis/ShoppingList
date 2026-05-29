# e-listamou.gr 🛒

A feature-rich, Full-Stack shopping list application built with **.NET Web API** and **React**, engineered with enterprise-level architecture patterns and production-ready optimizations.

🔗 **Live Demo:** [https://e-listamou.gr](https://e-listamou.gr)

## 🌟 Key Features & Architecture
- **Multi-Tenancy:** Engineered from the ground up to support isolated user/group spaces.
- **Secure Authentication:** Integrated OAuth2 flow utilizing Google Auth.
- **Optimistic UI Updates:** Smooth, lag-free user experience on the frontend by predicting server responses for state updates.
- **Per-Item Database Saving Optimization:** Minimizes database overhead and connection locks through highly optimized transactional updates.

---

## 🛠️ Tech Stack & Architecture

### Backend
- **Framework:** C# .NET 10 (ASP.NET Core Web API)
- **Database ORM:** Entity Framework Core (Code-First approach)
- **Real-Time Communication:** ASP.NET Core SignalR
- **Database:** PostgreSQL

### Frontend
- **Library:** React (Functional components, Hooks)
- **Styling:** Tailwind CSS
- **State Management:** Context API & Optimized Local State for reactive flows

### DevOps & Infrastructure
- **Containerization:** Docker & Docker Compose
- **Hosting:** Railway (Automated CD via GitHub Integration)
- **Network & DNS:** Cloudflare (SSL/TLS configuration and edge caching)

---

## 🧠 Technical Challenges & Decisions

### 1. Handling Network Latency (Optimistic UI)
* **Challenge:** Waiting for server and database validation on rapid user actions (e.g., checking 10 items off a list in succession) caused a sluggish user experience with visible delays.
* **Solution:** Implemented **Optimistic Updates** on the React frontend. The UI updates state instantly assuming success, while the network request executes in the background. If the API fails, a rollback mechanism reverts the UI to the last known valid server state.

### 2. Industry-Standard Authentication
* **Challenge:** Rolling out custom user credential storage introduces high security risks regarding hashing, token expiration, and credential leaks.
* **Solution:** Integrated **Google OAuth 2.0** to handle authentication securely via token exchange, removing the need to manage sensitive user credentials directly.

### 3. Automated CI/CD Pipeline & Production Deployment (Railway & Cloudflare)
* **Challenge:** Deploying a multi-container full-stack application traditionally requires tedious virtual server (VPS) configuration, manual SSL management, and reverse proxy setup, which slows down deployment iterations.
* **Solution:** Automated the publishing pipeline by linking the GitHub repository directly to **Railway** for seamless, hands-off Continuous Deployment (CD). Configured environment secrets at the infrastructure layer and routed traffic through **Cloudflare** to handle custom domains, enforce strict SSL/TLS encryption, and add edge networking security.

---

## 🗺️ Product Roadmap

This project has reached its core feature-freeze (MVP). Current status and future planned iterations include:

- [x] Core RESTful API & Multi-tenancy Data Isolation
- [x] Real-time asynchronous list sharing via SignalR Hubs
- [x] Optimistic UI Updates in React for lag-free performance
- [x] Multi-container Dockerization & Production Deployment
- [ ] **Smart AI Suggestions:** Integrating LLM capabilities to auto-generate shopping lists based on historical household usage.
- [ ] **Expense Analytics Dashboard:** Advanced React charts for tracking monthly spending trends per category.

