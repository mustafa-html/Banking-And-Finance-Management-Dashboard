# Banking and Finance Management Dashboard (Next.js + Appwrite)

## Summary
A full-stack fintech-style banking app that supports authentication, connecting bank accounts, viewing balances and transactions, and sending transfers using third-party financial integrations. Built to practice real-world patterns like secure auth, server actions, API workflows, and a clean responsive UI.


---

## ✨ Features
- **Authentication** — secure sign up/sign in with validation and protected routes
- **Connect Bank Accounts** — link multiple accounts using **Plaid**
- **Account Overview** — total balance, recent activity, category summaries
- **My Banks** — view all linked institutions and account details
- **Transaction History** — pagination + filtering for transaction lists
- **Transfers** — send funds via **Dwolla** with required recipient/account details
- **Responsive UI** — works smoothly on desktop, tablet, and mobile
- **Reusable Components** — modular UI + shared utilities for faster development

---

## 🧩 Architecture Overview
1. User authenticates (session stored securely).
2. User links a bank account with Plaid Link
3. The app exchanges Plaid public token → access token and fetches account metadata.
4. The app creates/updates records in Appwrite (users, banks, transactions).
5. When transferring funds:
   - Create a Dwolla customer/funding source (via Plaid processor token)
   - Submit a transfer request and store the transaction result.
6. UI revalidates/refreshes to show updates across pages.

---


---

## ⚙️ Tech Stack
- **Next.js**
- **TypeScript**
- **TailwindCSS**
- **Appwrite**
- **Plaid**
- **Dwolla**
- **React Hook Form**
- **Zod**
- **Chart.js**
- **shadcn/ui**

---

## ⚙️ Prerequisites
- Node.js (recommended: 18+)
- npm
- Git

---

## 🚀 Setup & Installation

### 1️⃣ Install dependencies
```bash
npm install
