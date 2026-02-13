# Snurr Revamp - Casino Management System

A comprehensive casino management system with a modern Next.js frontend and a robust Django REST Framework backend.

## 🚀 Overview

This project is a full-stack web application designed for casino management, featuring a wide range of modules including user management, payments, games, bonuses, loyalty programs, and more. It is built with a decoupled architecture, using **Django** for the backend API and **Next.js** for the frontend user interface.

## 🏗️ Project Structure

The project is organized into two main directories:

- **`backend/`**: Contains the Django REST Framework application handling all business logic, database interactions, and API endpoints.
- **`frontend/`**: Contains the Next.js application providing the interactive user interface and consuming the backend APIs.

---

## 🔧 Backend (Django)

The backend is built with **Django 6.0** and **Django REST Framework**, providing a secure and scalable API.

### Key Technologies
- **Framework:** Django 6.0
- **API:** Django REST Framework 3.16.1
- **Authentication:** JWT (Simple JWT)
- **Database Support:** PostgreSQL / MySQL
- **Environment Management:** Python Decouple

### Key Modules
- **Users & Permissions:** accounts, users, permissions_app, admin_app
- **Financials:** payments, transactions, wallets
- **Gaming:** games, wagers, bonuses, missions, loyalty
- **System:** activity_log, notifications, settings_app, support

### 🛠️ Backend Setup

1.  **Navigate to the backend directory:**
    ```bash
    cd backend
    ```

2.  **Activate Virtual Environment:**
    ```bash
    # Windows
    .\.venv\Scripts\Activate.ps1
    # Linux/Mac
    source .venv/bin/activate
    ```

3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run Migrations:**
    ```bash
    python manage.py migrate
    ```

5.  **Create Superuser (Optional):**
    ```bash
    python manage.py createsuperuser
    ```

6.  **Run Development Server:**
    ```bash
    python manage.py runserver
    ```
    The API will be available at `http://127.0.0.1:8000/`.

    The API will be available at `http://127.0.0.1:8000/`.

---

## 🐳 Docker (Full Stack)

You can run the entire application stack (Frontend, Backend, and Database) using Docker Compose.

1.  **Start the services:**
    ```bash
    docker-compose up --build
    ```

    This will start:
    -   **Backend:** `http://localhost:8000`
    -   **Frontend:** `http://localhost:3000`
    -   **PostgreSQL:** `localhost:5432`

2.  **Run Migrations (First Time Only):**
    Open a new terminal and run:
    ```bash
    docker-compose exec backend python manage.py migrate
    ```

3.  **Create Superuser (Optional):**
    ```bash
    docker-compose exec backend python manage.py createsuperuser
    ```

4.  **Stop the services:**
    ```bash
    docker-compose down
    ```

---

## 🎨 Frontend (Next.js)

The frontend is a modern web application built with **Next.js 16** using the App Router for optimal performance and SEO.

### Key Technologies
- **Framework:** Next.js 16 (App Router)
- **Library:** React 19
- **Styling:** Tailwind CSS v4
- **HTTP Client:** Axios
- **Forms:** React Hook Form
- **Utilities:** Date-fns, Recharts, React Icons

### 🛠️ Frontend Setup

1.  **Navigate to the frontend directory:**
    ```bash
    cd frontend
    ```

2.  **Install Dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Run Development Server:**
    ```bash
    npm run dev
    # or
    yarn dev
    ```
    The application will be available at `http://localhost:3000/`.

---

## 📝 Environment Variables

Both the backend and frontend rely on environment variables for configuration.

- **Backend:** Ensure a `.env` file exists in the `backend/` directory with necessary database credentials and secret keys.
- **Frontend:** Ensure environment variables (e.g., API base URL) are configured, typically in a `.env.local` file.

## 🤝 Contribution

1.  Fork the repository.
2.  Create a new branch for your feature (`git checkout -b feature/MyFeature`).
3.  Commit your changes (`git commit -m 'Add MyFeature'`).
4.  Push to the branch (`git push origin feature/MyFeature`).
5.  Open a Pull Request.
