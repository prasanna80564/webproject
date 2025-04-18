# 🏋️‍♂️ Fit Track Hub - Gym Management System

Fit Track Hub is a full-stack gym management system designed to simplify operations for fitness centers, trainers, and gym members. This web-based platform allows users to register, manage availability, track sessions, and for admins to monitor gym activities efficiently.

---

## 🚀 Features

- 🔐 **User Authentication** (JWT-based)
- 📅 **Workout Availability Management**
- 🧑‍💼 **Admin Dashboard** for member and session tracking
- 🧮 **Role-Based Access Control** (User/Admin/Moderator)
- 🗃️ **MongoDB with Mongoose ORM**
- 📈 **Request Logging & Monitoring**
- ⚙️ **Modular Service Architecture**
- 🧪 **Joi-based Request Validation**

---

## 🛠️ Tech Stack

| Layer            | Technologies                     |
|------------------|----------------------------------|
| **Frontend**     | HTML5 Templates (for responses)  |
| **Backend**      | Node.js, Express.js              |
| **Database**     | MongoDB, Mongoose ORM            |
| **Authentication** | JWT, bcryptjs                  |
| **Validation**   | Joi                              |
| **Logging**      | Morgan, Custom Middleware        |
| **Cache**        | NodeCache                        |
| **Environment**  | dotenv                           |

---


---

## 📡 API Endpoints

### 🔐 Auth Routes
| Method | Route                        | Description                |
|--------|------------------------------|----------------------------|
| POST   | `/api/v2/auth/signup`        | Register new user          |
| POST   | `/api/v1/auth/login`         | Login with email/password  |
| GET    | `/api/v1/auth/users`         | View all users (Admin)     |

### 🗓️ Member Availability Routes

| Method | Route                                      | Description                                                                 |
|--------|--------------------------------------------|-----------------------------------------------------------------------------|
| GET    | `/api/v1/member-availability`              | Retrieve submitted availability data for upcoming sessions. Supports filters by role, status, or assignment. |
| POST   | `/api/v1/member-availability`              | Submit new availability, specifying hours, date, workout type, or trainer assignment. |
| PUT    | `/api/v1/member-availability/:id`          | Edit existing availability records — adjust times, session types, or assigned trainers. |
| DELETE | `/api/v1/member-availability/:id`          | Delete outdated or incorrect availability entries (accessible by member or admin). |

---

## 🔒 Security Features

- Password hashing with `bcryptjs`
- JWT-based token authentication
- Input validation with `Joi`
- Role-based route protection
- .env file for secure secrets management
- Request logging and audit trail via MongoDB

---

## 🧪 Testing

Use **Postman** or **Thunder Client** to test routes. Sample request bodies are available in the `/test` folder or can be generated via Faker APIs integrated into the system.

---

## 🧭 Future Enhancements

- Full frontend dashboard with React.js + Tailwind CSS
- Admin analytics panel (charts and insights)
- Class schedule calendar for users
- Email/OTP-based login security
- Docker container support for deployment

---

## 📦 Installation & Setup

```bash
# Clone the repository
git clone https://github.com/Selvarani-21/webproject.git
cd fit-track-hub

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env

# Start the development server
npm run dev