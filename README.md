# 🌱 Web-Based E-Commerce Platform for Plant Nursery  

A full-stack web-based e-commerce application designed for an online **Plant Nursery**, enabling users to browse plants, search products, authenticate securely, and place orders through a scalable microservice-based backend.

## 🧱 Project Structure

```text
WebBasedEcommerceForPlantNursery/
│
├── client/                    # Frontend (React)
│   ├── public/
│   └── src/
│       ├── actions/
│       ├── api/
│       ├── components/
│       ├── reducers/
│       └── styles/
│
├── server/                    # Backend (Microservices)
│   ├── authentication-service/
│   ├── common-data-service/
│   └── search-suggestion-service/
│
├── mysql-db/
│   └── user.sql               # Database schema
│
├── docker-compose.yml         # Service orchestration
├── start-all.sh               # Start all services
├── stop-all.sh                # Stop all services
└── README.md
```

## 🎥 Demo
> ⏳ *Waiting for finalization*

## ✨ Features

- 🔐 Google OAuth 2.0 for quick login
- 👤 Username / Password authentication
- 🔍 Smart search with real-time suggestions
- 🗄️ User & product data stored in **MySQL**
- ⚡ API caching using **Redis** to reduce network calls
- 🎛️ Filters for categories and product attributes
- 📊 Sorting by popularity, newest, and price
- 📄 Pagination for optimized product display
- 🍪 Authentication tokens stored in cookies
- 🛒 Cart data stored in cookies
- 💳 Secure payments using **Stripe API**
- 📱 Fully responsive across all devices

## 🧰 Tech Stack

### 🖥 Frontend
- ⚛️ ReactJS
- 🎨 Material-UI
- 🧩 Semantic-UI
- 🧠 Redux
- 🌐 Axios

### 🔧 Backend
- ☕ Spring Boot 2.0
- 🌱 Spring REST Controller
- 🗃️ Spring Data JPA

### 🗄 Database & Caching
- 🐬 MySQL
- ⚡ Redis

### ☁️ Cloud & Services
- ☁️ Cloudinary (Image CDN)
- 🔐 Google OAuth 2.0
- 💳 Stripe Payment Gateway
- 🚀 Heroku Cloud Platform

### 🐳 DevOps
- 🐳 Docker
- 🧩 Docker Compose

## 🧱 Microservices Architecture

### 🔹 Services Overview

- **🖥 React-UI Service**  
  Frontend client that renders UI and communicates with backend services via REST APIs.

- **📦 Common Data Service**  
  Manages products, categories, filters, and order-related data.

- **🔐 Authentication Service**  
  Handles user registration, login, OAuth authentication, and token management.

- **💳 Payment Service**  
  Processes payment requests and interacts with the Stripe API.

- **🔍 Search Suggestion Service**  
  Provides prefix-based search suggestions using a HashMap built from database data.

## 🧠 Architecture Overview

The application follows a **distributed microservices architecture**, ensuring scalability, fault isolation, and independent deployments.

---

## 📊 Architecture Diagram (Logical Flow)

```text
[ Browser ]
     |
     v
[ React UI ]
     |
     v
[ API Gateway / REST Calls ]
  |        |        |        |
  v        v        v        v
Auth   Common   Search   Payment
Svc     Data     Svc       Svc
   \       |        |       /
            v
         MySQL
            |
          Redis
```

2️⃣ Configure Environment Variables (Optional)

⚠️ The app runs without these, but Payment & OAuth will be disabled.

REACT_APP_STRIPE_PUBLISH_KEY=<Your Stripe Publishable Key>
REACT_APP_GOOGLE_AUTH_CLIENT_ID=<Your Google OAuth Client ID>


🔗 Create accounts:

Stripe: https://dashboard.stripe.com/register

Google OAuth: https://console.developers.google.com

3️⃣ Build & Start All Services
./start-all.sh


This will:

Build all microservices

Create Docker network

Start containers based on docker-compose.yml

4️⃣ Stop Services
./stop-all.sh


Use this when making code changes.

💳 Payment Service Test Details
Card Number: 4242 4242 4242 4242
Expiry Date: Any future date
CVV: Any 3-digit number

🚀 Deployment on Heroku

Create heroku.yml (Docker-based deployment)

Add MySQL from Heroku Marketplace

💡 Requires credit/debit card (free tier available)

Configure database environment variables

Set container stack:

heroku stack:set container -a <application-name>


Deploy individual microservices

📚 References

Spring CORS Support

Heroku Docker Builds

Material-UI

Semantic UI

Redis Commands

Spring Data Redis

Stripe Docs

Google OAuth Docs

Redux & React Hooks

## ❤️ Contributions
Contributions are welcome!
> Fork the repo → Create a branch → Add feature → Submit PR

</br></br>
<div align="center">
<p>📘 This project is created strictly for educational and learning purposes.</p>
<p>⭐ If you find this project helpful, feel free to star the repository!</p>
<p>© 2026 <strong><a href = "https://bemaurya.github.io">BeMaurya</a></strong>. All rights reserved.</p>
</div>
