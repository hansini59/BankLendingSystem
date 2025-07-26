# 💰 Bank Lending System

This project is a full-stack implementation of a simple **Bank Lending System**, built for the Agetware assignment. It includes a React.js frontend, a Node.js + Express backend, and a SQL database (SQLite/PostgreSQL) for persistence.

---

## 🧱 Project Structure

```
/bank-lending-system
├── backend/           # Node.js + Express API
│   ├── index.js
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   └── db/
├── frontend/          # React frontend
│   ├── public/
│   └── src/
└── README.md
```

---

## 🚀 Features

- Create and track **loans**
- Record **EMI / lump sum payments**
- Generate **ledgers** for each loan
- View **customer-wise account overviews**
- **RESTful API design**
- **Simple interest** calculations
- Modular code structure

---

## ⚙️ Tech Stack

| Layer           | Technology         |
|----------------|--------------------|
| Frontend       | React.js           |
| Backend        | Node.js, Express.js|
| Database       | SQLite / PostgreSQL|

---

## 📦 Installation

### 1️⃣ Clone the Repo

```bash
git clone https://github.com/hansini59/BankLendingSystem.git
cd BankLendingSystem
```

---

### 2️⃣ Backend Setup

```bash
cd backend
npm install
# Create .env file for DB settings if needed
node index.js
```

- Runs Express API at: `http://localhost:5000`
- Default DB: SQLite or configure PostgreSQL in `.env`

---

### 3️⃣ Frontend Setup

```bash
cd ../frontend
npm install
npm start
```

- Runs React frontend at: `http://localhost:3000`

---

## 🧪 Sample API Endpoints

> Base URL: `/api/v1`

| Method | Endpoint                             | Description                      |
|--------|--------------------------------------|----------------------------------|
| POST   | `/loans`                             | Create a new loan                |
| POST   | `/loans/:loan_id/payments`           | Make a payment                   |
| GET    | `/loans/:loan_id/ledger`             | View loan ledger                 |
| GET    | `/customers/:customer_id/overview`   | View all loans for a customer    |

---

## 🧮 EMI & Interest Logic

- Simple Interest: `I = P × N × R / 100`
- Total Amount: `A = P + I`
- Monthly EMI: `A / (N × 12)`

---

## 🛠️ Database Schema

### 🧑 Customers
- `customer_id` (PK)
- `name`
- `created_at`

### 💸 Loans
- `loan_id` (PK)
- `customer_id` (FK)
- `principal_amount`
- `total_amount`
- `interest_rate`
- `monthly_emi`
- `loan_period_years`
- `status`
- `created_at`

### 💳 Payments
- `payment_id` (PK)
- `loan_id` (FK)
- `amount`
- `payment_type` (`EMI` / `LUMP_SUM`)
- `paid_on`

---

## 🌐 Deployment

### 🔹 Vercel / Netlify (Frontend)

1. Go to (https://vercel.com/musku-hansinis-projects/bank-lending-system/HXpLmmgijxU5tJum3n3xBcgEukUn)
2. Import the frontend project from GitHub
3. Set `build command` as: `npm run build`
4. Set `output directory` as: `build`
5. Deploy and get your live URL!


---

## 👩‍💻 Author

**Hansini Musku**  
Frontend & Full-Stack Developer  
🔗 GitHub: [@hansini59](https://github.com/hansini59)

---

