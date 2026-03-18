# 📘 Job Board App – Full-Stack Web Application

A complete **Job Board Application** where users can view jobs, and admins can log in to post, edit, and delete job listings.

This project is built using a **full-stack architecture with React, Node.js, Express, and MySQL**, including authentication and protected routes for admin access.

---

# 🚀 Live Demo

* 🌐 **Frontend Live Site:** https://job-board-gorav.netlify.app
* 🔗 **Backend API:** https://job-board-api.onrender.com

---

# 🛠 Tech Stack

| Layer          | Technology                |
| -------------- | ------------------------- |
| Frontend       | React, Context API, Axios |
| Backend        | Node.js, Express.js       |
| Database       | MySQL (XAMPP)             |
| Authentication | JWT, bcrypt               |
| Styling        | CSS                       |
| Deployment     | Netlify + Render          |

---

# 📁 Folder Structure

```bash
job-board-app/
│
├── backend/
│   ├── routes/
│   │   └── jobs.js
│   │
│   ├── middleware/
│   │   └── authMiddleware.js
│   │
│   ├── db.js
│   ├── auth.js
│   ├── index.js
│   ├── hashPassword.js
│   └── package.json
│
├── frontend/
│   └── src/
│       ├── api.js
│       │
│       ├── components/
│       │   ├── AdminDashboard.js
│       │   ├── AdminJobs.js
│       │   ├── JobForm.js
│       │   ├── JobList.js
│       │   ├── JobFilters.js
│       │   ├── Login.js
│       │   ├── Register.js
│       │   ├── Navbar.js
│       │   └── Spinner.js
│       │
│       ├── contexts/
│       │   └── AuthContext.js
│       │
│       ├── App.js
│       ├── index.js
│       └── styles.css
```

---

# 🔐 Authentication Features

* JWT-based authentication
* Admin role-based access control
* Protected frontend routes using Context API
* Secure cookie handling with **httpOnly cookies**

---

# 📦 Backend Setup

```bash
cd backend
npm install
npm start
```

## ✅ Environment Variables (.env)

```env
PORT=4000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=jobboard
JWT_SECRET=yourSecretHere
```

---

# 🔑 Manual Admin Password Hashing

To manually generate a hashed password:

```bash
node hashPassword.js yourpassword
```

Then insert the generated hash into MySQL:

```sql
INSERT INTO users (username, password, isAdmin)
VALUES ('admin', '<paste_hash_here>', 1);
```

---

# 🌐 Frontend Setup

```bash
cd frontend
npm install
npm start
```

---

# 🔌 Axios Configuration

## frontend/src/api.js

```javascript
import axios from 'axios';

const api = axios.create({
  baseURL: 'http://localhost:4000/api',
  withCredentials: true,
});

export default api;
```

---

# 📚 Core Functionalities

## ✅ Admin Features

* Login / Logout
* Add new job posts
* Edit existing jobs
* Delete jobs
* Protected admin dashboard

## ✅ User Features

* View all available jobs
* Filter jobs by:

  * Title
  * Location
  * Job Type

## ✅ Authentication Flow

* `POST /api/auth/login` → Login & get JWT token
* `GET /api/auth/me` → Validate token & fetch current user
* `POST /api/auth/logout` → Clear cookie & logout

---

# 📂 Important Files Explained

## Backend

* **auth.js** → Login / Register / Logout APIs
* **authMiddleware.js** → JWT verification middleware
* **hashPassword.js** → Password hashing utility
* **jobs.js** → CRUD operations for jobs
* **db.js** → MySQL connection setup

## Frontend

* **AuthContext.js** → Authentication state management
* **AdminDashboard.js** → Admin job management panel
* **JobForm.js** → Create / Edit job form
* **JobList.js** → Public job listing page
* **JobFilters.js** → Search and filter jobs
* **Navbar.js** → Dynamic navbar based on auth state
* **Spinner.js** → Loading indicator

---

# 📸 Screenshots

Save screenshots inside:

```bash
frontend/public/screenshots/
```

Recommended screenshots:

* 🔐 Login Page
* 👤 Admin Dashboard
* 📄 Job Listing
* 🎯 Filters UI

---

# 🚀 Future Improvements

* Pagination
* Email notifications
* Resume upload feature
* Admin user management
* Search optimization
* Job application tracking

---

# ✅ Project Highlights

* Full authentication flow implemented
* Admin-only protected routes
* Clean folder structure
* Production-ready API integration
* Scalable architecture

---

# 👨‍💻 Author

**Gorav Gumber**

---

# ⭐ If you like this project

Give it a **star on GitHub** and connect for more full-stack projects 🚀
