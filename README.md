# Tommo 🐻

> A collaborative household expense management web application

**Tommo** helps families and friends manage shared expenses in one place.  
It provides real-time expense tracking and a voting system for making spending decisions together.

---

## 🧩 Problem

- Shared finances are hard to manage when expenses are tracked individually
- Verbal agreements or messengers often lead to misunderstandings
- Digital payments reduce awareness of actual spending
- **63% of people in their 20s and 30s report not knowing their exact monthly expenses**

---

## ✨ Key Features

- **Group Account Book**: Manage income and expenses with multiple members
- **Calendar View**: Monthly expense overview
- **Statistics & Charts**: Spending analysis by category
- **Voting System**: Vote on significant expenses
- **Social Features**: Comments, reactions, and notifications
- **Excel Export**: Download expense data

---

## 🛠️ Tech Stack

- **Frontend**: React, TypeScript, Vite
- **Styling**: Tailwind CSS, Framer Motion
- **State Management**: Zustand
- **Backend**: Supabase (PostgreSQL, Auth, Realtime, Storage)
- **Charts**: Recharts
- **Tools**: ESLint, Prettier

---

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/towmoo.git
cd towmoo
npm install
npm run dev

___

## 👤 My Role

- Implemented authentication using **Supabase OAuth**, supporting **Google and Kakao social login** only,
  based on a two-week development timeline and minimal user data requirements.

- Managed global user state with **Zustand**, as application access was determined by an `isAuth` flag
  and user data was shared across multiple components.

- Resolved **OAuth redirect timing issues** between Google and Kakao by storing a temporary flag in
  `localStorage` during login and handling post-login UI feedback in the `Layout` component.

- Fixed an **infinite API call issue** caused by duplicated fetch logic in child components
  by lifting the data-fetching logic to the parent component and passing data via props.

---

<img width="2048" height="2048" alt="Towmoo Logo" src="https://github.com/user-attachments/assets/0c3ddbb4-c9e0-4bc0-a4ed-c6db4fa8086d" />

