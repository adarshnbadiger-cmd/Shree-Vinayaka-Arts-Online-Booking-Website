# Shree Vinayaka Arts - Online Booking Website

Production-oriented Ganesha idol booking website for Shree Vinayaka Arts, Gadag.

## Features
- Divine, festive UI with English and Kannada support.
- Full Razorpay integration (100% payment required).
- Real-time stock reservation to prevent overbooking.
- Secure Admin Dashboard for product and booking management.

## Tech Stack
- Frontend: React, Vite, TypeScript, Tailwind CSS
- Backend: Node.js, Express, MongoDB, TypeScript
- Payments: Razorpay

## Setup Instructions

### 1. MongoDB
Ensure MongoDB is running locally on `mongodb://localhost:27017/shree_vinayaka_arts`.

### 2. Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your Razorpay keys and session secret
npm run dev
```

### 3. Create First Admin
```bash
cd backend
npx ts-node tools/create-admin.ts admin@example.com mypassword "Admin Name"
```

### 4. Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

## Razorpay Configuration
1. Log in to Razorpay Dashboard -> Settings -> API Keys.
2. Generate Test Key ID and Secret.
3. Add them to `backend/.env`.
4. Configure a Webhook for `payment.captured` pointing to `http://your-domain/api/payments/webhook`.

## Project Structure
- `/backend`: API, Database Models, Payment Logic
- `/frontend`: React Client, i18n, Admin UI
