# 🌾 AgroShare — Farm Equipment Rental Platform

AgroShare is a full-stack web application that connects farmers, equipment owners, and transport helpers to simplify agricultural equipment rental in rural India.

---

## 🚀 Features

- **Farmers** can browse and rent farm equipment, track rental status, and make payments
- **Owners** can list equipment, approve/reject rental requests, and assign transport
- **Transport Helpers** can register their vehicle and accept/reject delivery requests
- **Admin** can manage all users, equipment, and view revenue analytics
- **Razorpay** payment integration (online + cash on delivery)
- JWT-based authentication with role-based access control

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React.js, Vite, Axios |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Auth | JWT (JSON Web Tokens) |
| Payments | Razorpay |
| File Uploads | Multer |
| Deployment | Vercel (frontend), Render (backend) |

---

## 📁 Project Structure

```
AgroShare/
├── backend/
│   ├── middleware/       # auth, admin, upload, errorHandler
│   ├── models/           # User, Equipment, Rental, TransportRequest
│   ├── routes/           # authRoutes, equipmentRoutes, rentalRoutes, etc.
│   └── server.js
├── frontend/
│   ├── src/
│   │   ├── components/   # Navbar, Footer, ProtectedRoute, etc.
│   │   ├── context/      # AuthContext (useReducer)
│   │   ├── pages/        # All page components
│   │   └── api.js        # Axios instance with interceptors
│   └── index.html
└── README.md
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Node.js v18+
- MongoDB Atlas account (or local MongoDB)
- Razorpay test account

### Backend

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` folder:

```env
MONGO_URI=your_mongodb_connection_string
PORT=5000
JWT_SECRET=your_secret_key
RAZORPAY_KEY=your_razorpay_key
RAZORPAY_SECRET=your_razorpay_secret
```

```bash
npm run dev
```

### Frontend

```bash
cd frontend
npm install
```

Create a `.env` file in the `frontend/` folder:

```env
VITE_API_URL=http://localhost:5000/api
VITE_RAZORPAY_KEY=your_razorpay_key
```

```bash
npm run dev
```

Open `http://localhost:5173` in your browser.

---

## 👥 User Roles

| Role | Capabilities |
|------|-------------|
| Farmer | Browse equipment, create rentals, pay, rate |
| Owner | List equipment, approve rentals, assign transport |
| Transport | View and accept delivery requests |
| Admin | Full dashboard, analytics, user & equipment management |

---

## 📸 Screenshots

<img width="1910" height="947" alt="image" src="https://github.com/user-attachments/assets/c4e322a2-199f-4bbe-9328-3e0afa9237e6" />
<img width="1914" height="936" alt="image" src="https://github.com/user-attachments/assets/3ec5d07c-d230-4ac8-9dad-c587e9023764" />
<img width="1900" height="932" alt="image" src="https://github.com/user-attachments/assets/a6bf138a-8e10-47f4-b17d-7ffec69c0788" />
<img width="1906" height="947" alt="image" src="https://github.com/user-attachments/assets/999d2e0e-a1e2-49f8-973f-308b17139daa" />
<img width="1079" height="941" alt="image" src="https://github.com/user-attachments/assets/f47c7daf-c1d3-4c6e-8a46-965a31681fd2" />
<img width="1876" height="945" alt="image" src="https://github.com/user-attachments/assets/a38a70a3-cc30-40cd-b02c-b9babcb4e1c2" />

---

## 🔐 Security Features

- Passwords hashed with bcryptjs
- JWT authentication on all protected routes
- Input validation using express-validator
- Razorpay payment signature verification
- `.env` secrets never committed to Git

---

## 👩‍💻 Author

**Bindu Chinta**  
GitHub: https://github.com/Bindu2419
