OLL Business Bootcamp Frontend

This is the React + TypeScript frontend for the OLL Business Bootcamp Platform, built for students, mentors, and admins to interact with the learning, sales, and mentoring ecosystem. It features role-based routing, reusable UI components, and scalable architecture for business bootcamp management.

🔧 Tech Stack
React – Frontend framework

TypeScript – Type safety & better DX

Vite – Fast build tool

Tailwind CSS – Utility-first styling

shadcn/ui – Component library for consistent UI

Lucide React – Icon library

React Router DOM – Role-based routing

TanStack Query – Data fetching & server state management

📁 Project Structure
bash
Copy
Edit
/src
├── components          # Reusable components
│   ├── ui              # shadcn/ui components
│   └── ui-custom       # App-specific custom UI
├── hooks               # Custom React hooks
├── lib                 # Utility functions & helpers
├── pages               # Page components grouped by user role
│   ├── student/
│   ├── mentor/
│   └── admin/
├── App.tsx             # Main routing with role-based routes
🔐 Role-Based Routing
Each user role has a dedicated route structure:

Student – Tasks, Sales, Sessions, Leaderboard, Feedback

Mentor – Batch Management, Earnings, Sessions

Admin – Program Management, Revenue, User Management

Routing is handled in App.tsx.

🚀 Key Features
Public Pages
Landing Page – Hero section, testimonials, CTA

Login / Register – Role selection & authentication

Student
Dashboard, Tasks, Sessions, Sales, Leaderboard, Feedback, Reviews, Profile, Help

Mentor
Dashboard, Batches, Earnings, Sessions, Leaderboard, Profile

Admin
Dashboard, Batches, Students, Teachers, Earnings, Feedback, Profile

🧩 Components
Layout Components
MainLayout – Authenticated pages layout

Sidebar – Collapsible navigation with role switcher

UI & Custom Components
Built using shadcn/ui

UserAvatar, ProgressCard, TaskCard for dynamic UI rendering

🔄 State & Data Management
Local State – React’s useState

Server State – TanStack Query

Routing Params – Used for dynamic page behavior

🌐 API Integration (Expected)
Module	Endpoint
Auth	/api/auth/login, /api/auth/register
Students	/api/students/{id}/tasks, /sales
Mentors	/api/mentors/{id}/batches, /earnings
Admin	/api/admin/batches, /students
Common	/api/tasks, /leaderboard, /sessions

All endpoints are expected to return data matching mock structures used in components.

🧪 Testing Strategy
Component Testing – Isolated shadcn/ui components

Integration Testing – Role-based flows

Mock Data – Used for all pages (replace with APIs on backend integration)

🔐 Authentication & Access
JWT Auth with role included in token

Role-Based Middleware for protected routes

Access Control to restrict page access by role

📦 Setup Instructions
# Clone the repo
git clone https://github.com/your-org/oll-bootcamp-frontend.git
cd oll-bootcamp-frontend
# Install dependencies
npm install
# Start dev server
npm run dev


🤝 Contribution Guide
Use consistent folder and naming conventions

Ensure components are reusable and role-agnostic if possible

Always write meaningful commit messages

Use prettier and eslint before pushing

📬 Contact
For support or feature requests, please reach out to the OLL Dev Team or open an issue on GitHub.
