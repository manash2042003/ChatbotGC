HR-Employee Chatbot System
Project Description
The HR-Employee Chatbot System is an AI-powered solution designed to enhance employee engagement and well-being tracking. It integrates multiple datasets (e.g., Vibemeter, performance reviews, leave records) to identify employees requiring engagement, conduct personalized conversations, and provide actionable insights for HR teams. The system automates HR workflows, reduces manual effort, and fosters a positive workplace culture.

Key Features
SHAP Integration: Identifies employees requiring engagement based on SHAP values.
Personalized Conversations: Context-aware chatbot interactions powered by GPT-4.
Sentiment Analysis: Real-time emotion detection using DistilBERT.
HR Dashboard: Displays analytics, flagged employees, and detailed reports.
Automated Reporting: Generates daily and employee-specific reports.
Tech Stack
Frontend
Framework: Next.js
Styling: TailwindCSS
Deployment: Vercel
Backend
Framework: FastAPI
Database: PostgreSQL
AI Models: GPT-4, DistilBERT
Deployment: Render
Steps to Run the Project
Prerequisites
Node.js (v16+): Download
Python (v3.9+): Download
PostgreSQL: Install and configure a PostgreSQL database
Environment Variables: Create .env files for both frontend and backend
Backend Setup
Clone the Repository:

git clone https://github.com/your-repo/hr-employee-chatbot.git
cd hr-employee-chatbot/Server
Create a Virtual Environment:

python3 -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows
Install Dependencies:

pip install -r requirements.txt
Set Up Environment Variables:
Create a .env file in the Server directory:

DATABASE_URL=postgresql://<username>:<password>@localhost:5432/<database_name>
OPENAI_API_KEY=<your_openai_api_key>
AWS_ACCESS_KEY_ID=<your_aws_access_key>
AWS_SECRET_ACCESS_KEY=<your_aws_secret_key>
Run Database Migrations:

alembic upgrade head
Start the Backend Server:

uvicorn main:app --reload
The backend will be available at: http://127.0.0.1:8000

Frontend Setup
Navigate to the Frontend Directory:

cd ../client
Install Dependencies:

npm install
Set Up Environment Variables:
Create a .env.local file:

NEXT_PUBLIC_API_BASE_URL=http://127.0.0.1:8000
Start the Frontend Server:

npm run dev
The frontend will be available at: http://localhost:3000

Backend Setup
Navigate to the Backend Directory:

cd server
Create a Virtual Environment:

python -m venv venv
Activate the Virtual Environment:

venv/bin/activate  # Use `venv\Scripts\activate` on Windows
Install Dependencies:

pip install -r requirements.txt
Start the Backend Server:

uvicorn main:app --reload
The backend will be available at: http://127.0.0.1:8000

Testing the System
Access the Frontend:
Open http://localhost:3000 in your browser.

API Documentation:
Visit http://127.0.0.1:8000/docs (Swagger UI) for testing APIs.

Database:
Use a tool like pgAdmin to manage and inspect the PostgreSQL database.

Deployment
Frontend (Vercel)
Push the client directory to a GitHub repository.
Connect the repo to Vercel and deploy.
Backend (Render)
Push the Server directory to a GitHub repository.
Connect the repo to Render and deploy.
