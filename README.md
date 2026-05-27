# e-listamou.gr 🛒

A feature-rich, Full-Stack shopping list application built with **.NET Web API** and **React**, engineered with enterprise-level architecture patterns and production-ready optimizations.

🔗 **Live Demo:** [https://e-listamou.gr](https://e-listamou.gr)

## 🌟 Key Features & Architecture
- **Multi-Tenancy:** Engineered from the ground up to support isolated user/group spaces.
- **Secure Authentication:** Integrated OAuth2 flow utilizing Google Auth.
- **Optimistic UI Updates:** Smooth, lag-free user experience on the frontend by predicting server responses for state updates.
- **Per-Item Database Saving Optimization:** Minimizes database overhead and connection locks through highly optimized transactional updates.

## 🛠️ Tech Stack
- **Frontend:** React.js, Tailwind CSS, State Management
- **Backend:** .NET Web API (C#), Entity Framework Core
- **Database:** PostgreSQL

## 🚀 Getting Started

### Prerequisites
- .NET 10.0 SDK
- Node.js & npm
- PostgreSQL

### Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/George-Daoutis/ShoppingList.git

3. Setup the backend:
   ```bash
   cd Backend
   dotnet restore
   dotnet run
   
5. Setup the frontend:
   ```bash
   cd Frontend
   npm install
   npm run dev
