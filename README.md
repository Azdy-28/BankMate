🏦 BankMate

BankMate is a state-of-the-art financial SaaS platform that connects to multiple bank accounts, displays real-time transactions, allows users to transfer money, and manage their finances—all in one place.

🚀 Features

🔐 Secure Authentication: SSR authentication with validations using Appwrite.

🏦 Connect Banks: Integrates with Plaid to link multiple real-world bank accounts.

📊 Dashboard: Visualizes total balance, recent transactions, and spending categories.

💸 Fund Transfers: Users can transfer money to other BankMate users using Dwolla.

📱 Responsive Design: Fully mobile-optimized UI using TailwindCSS and ShadCN.

🛠️ Tech Stack

Frontend: Next.js 14 (App Router), TypeScript, TailwindCSS, ShadCN UI.

Backend: Appwrite (Database, Auth), Server Actions.

Fintech APIs: Plaid (Banking Data), Dwolla (Payment Processing).

Form Handling: React Hook Form + Zod.

⚙️ Local Setup Instructions

1. Clone the Repository

git clone [https://github.com/Azdy-28/BankMate.git](https://github.com/Azdy-28/BankMate.git)
cd BankMate


2. Install Dependencies

npm install


3. Environment Variables

Create a .env file in the root directory and add the following keys:

# APPWRITE
NEXT_PUBLIC_APPWRITE_ENDPOINT="[https://cloud.appwrite.io/v1](https://cloud.appwrite.io/v1)"
NEXT_PUBLIC_APPWRITE_PROJECT="<YOUR_PROJECT_ID>"
APPWRITE_DATABASE_ID="<YOUR_DB_ID>"
APPWRITE_USER_COLLECTION_ID="<YOUR_USER_COLLECTION_ID>"
APPWRITE_BANK_COLLECTION_ID="<YOUR_BANK_COLLECTION_ID>"
APPWRITE_TRANSACTION_COLLECTION_ID="<YOUR_TRANSACTION_COLLECTION_ID>"
APPWRITE_SECRET="<YOUR_API_KEY>"

# PLAID (Sandbox)
PLAID_CLIENT_ID="<YOUR_PLAID_CLIENT_ID>"
PLAID_SECRET="<YOUR_PLAID_SANDBOX_SECRET>"
PLAID_ENV="sandbox"
PLAID_PRODUCTS="auth,transactions,identity"
PLAID_COUNTRY_CODES="US"

# DWOLLA (Sandbox)
DWOLLA_KEY="<YOUR_DWOLLA_KEY>"
DWOLLA_SECRET="<YOUR_DWOLLA_SECRET>"
DWOLLA_BASE_URL="[https://api-sandbox.dwolla.com](https://api-sandbox.dwolla.com)"
DWOLLA_ENV="sandbox"


4. Database Setup (Appwrite)

To run this project, ensure your Appwrite Database Collections have the following Attributes:

Users Collection:
email, firstName, lastName, address1, city, state, postalCode, dateOfBirth, ssn, userId (String).

Banks Collection:
userId, bankId, accountId, accessToken, fundingSourceUrl, shareableId.

Transactions Collection:
name, amount, channel, category, senderBankId, receiverBankId, date, type, bankId, userId.

5. Run the App

npm run dev


Open http://localhost:3000 in your browser.

🧪 Testing Credentials (Plaid Sandbox)

When linking a bank, use these credentials to simulate a successful connection:

Username: user_good

Password: pass_good

