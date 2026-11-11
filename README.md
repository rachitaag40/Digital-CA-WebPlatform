# Digital CA Platform

A full-stack web application designed to simplify the way **Chartered
Accountants (CAs) and clients connect and manage accounting-related
services**. The platform provides separate workspaces for CA
professionals and clients, bringing service requests, client management,
documents, tasks, and communication into one place.

## Project Goal

The goal of this project is to make CA-client interactions more
organized and accessible by replacing scattered communication and manual
service coordination with a centralized digital platform. Clients can
find CA professionals, request services, and track their requests, while
CAs can manage clients and handle day-to-day work through a dedicated
dashboard.

## Key Features

-   **Authentication and role-based access:** Registration, login, and
    separate experiences for CA and client accounts.
-   **CA dashboard:** A workspace for managing clients, service
    requests, tasks, documents, and account settings.
-   **Client dashboard:** A place for clients to find CAs, request
    services, track requests, manage documents, and update their
    profiles.
-   **Service request management:** Submit, manage, and track CA service
    requests.
-   **Document management:** Upload and access documents through the
    platform.
-   **Task management:** Organize CA-related tasks and work.
-   **Messaging:** Support communication between clients and CA
    professionals.
-   **Payments:** Stripe payment integration endpoints, including
    webhook handling.
-   **Reports and updates:** Dashboard/report views and a news and
    updates section.

## Worked On

I developed the platform as a full-stack project, working across its
frontend and backend:

-   Built React and TypeScript pages for the landing page,
    authentication, CA dashboard, client dashboard, profiles, service
    requests, documents, tasks, messages, reports, and settings.
-   Created separate CA and client user experiences with role-aware
    navigation and authentication context.
-   Developed the Node.js and Express backend with API routes,
    controllers, middleware, and MongoDB models.
-   Implemented backend functionality for authentication, CA/client
    management, service requests, documents, chat, dashboards, news, and
    payments.
-   Connected the frontend to the backend API and configured the local
    API fallback.
-   Added integrations/configuration for MongoDB, Stripe, AWS S3, and
    Cloudinary.

## Tech Stack

  Area                      Technologies
  ------------------------- ------------------------------------------------
  Frontend                  React, TypeScript, Vite
  UI and routing            React Router, CSS, Framer Motion, Lucide React
  Charts                    Recharts
  Backend                   Node.js, Express.js
  Database                  MongoDB, Mongoose
  Authentication            JWT, bcryptjs
  File handling             Multer
  Payments                  Stripe
  Additional integrations   AWS S3, Cloudinary

## Project Structure

``` text
CA web pro/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── config/
│   │   └── pages/
│   │       ├── ca/
│   │       └── user/
│   └── package.json
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── index.js
│   └── package.json
└── README.md
```

## Getting Started

### Prerequisites

-   Node.js and npm
-   MongoDB database (local or MongoDB Atlas)

### 1. Clone the repository

``` bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd "CA web pro"
```

### 2. Configure the backend

Create a `backend/.env` file and add the environment variables required
by the backend configuration. For example:

``` env
MONGODB_URI=your_mongodb_connection_string
PORT=5001
```

Add other required secrets for the services you configure, using the
variable names expected by the source code. **Never commit `.env` files
or real credentials to GitHub.**

### 3. Install and start the backend

``` bash
cd backend
npm install
npm run dev
```

The backend uses port `5001` by default.

### 4. Install and start the frontend

Open a second terminal:

``` bash
cd frontend
npm install
npm run dev
```

Vite will display the local frontend URL in the terminal. The frontend
uses `http://localhost:5001` as its default backend API URL. To change
it, configure `VITE_API_URL` in the frontend environment.

### Build the frontend

``` bash
cd frontend
npm run build
```

The production build is generated in `frontend/dist/`.

## Notes

-   MongoDB and any required third-party service credentials must be
    configured before using the corresponding backend features.
-   Stripe, AWS S3, and Cloudinary integrations require valid provider
    configuration.
-   The README describes the project structure and functionality found
    in the source code; individual features and external integrations
    should be tested in the configured environment before production
    use.
-   Keep `.env`, API keys, database credentials, and other secrets out
    of version control.

------------------------------------------------------------------------

**Digital CA Platform** --- Bringing CA professionals and clients
together through one organized digital workspace.
