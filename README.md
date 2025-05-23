
# OLL Business Bootcamp Frontend

A **React + TypeScript** web application for students, mentors, and admins to manage learning, mentoring, and sales workflows for the OLL Business Bootcamp.

---

## 🚀 Tech Stack

- **React** – UI library  
- **TypeScript** – Static typing  
- **Vite** – Lightning‑fast build tool  
- **Tailwind CSS** – Utility‑first styling  
- **shadcn/ui** – Accessible component library  
- **Lucide React** – Icon set  
- **React Router DOM** – Client‑side routing  
- **TanStack Query** – Data fetching & caching  

---

## 📁 Project Structure

```text
src/
├─ components/
│  ├─ ui/           # shadcn/ui primitives
│  └─ ui-custom/    # domain‑specific UI
├─ hooks/           # custom React hooks
├─ lib/             # helpers & utilities
├─ pages/           # routed pages (grouped by role)
│  ├─ student/
│  ├─ mentor/
│  └─ admin/
└─ App.tsx          # top‑level routing & providers
```

---

## 🔐 Role‑Based Routes

| Role    | Core Pages                                                          |
|---------|---------------------------------------------------------------------|
| Student | Dashboard · Tasks · Sessions · Sales · Leaderboard · Profile · Help |
| Mentor  | Dashboard · Batches · Sessions · Earnings · Leaderboard · Profile   |
| Admin   | Dashboard · Batches · Students · Teachers · Earnings · Feedback     |

Routing is declared in **`App.tsx`** and guards access with the user’s role.

---

## 🧩 Key Components

- **MainLayout** – Authenticated page shell (sidebar + outlet)  
- **Sidebar** – Collapsible navigation, role‑aware  
- **UserAvatar**, **ProgressCard**, **TaskCard** – Custom UI built on shadcn/ui  

---

## 🗄️ State & Data

| Layer        | Library        | Purpose                     |
|--------------|---------------|-----------------------------|
| Local        | `useState`    | Simple component state      |
| Server state | TanStack Query| Fetching, caching, syncing  |
| URL params   | React Router  | Contextual page data        |

---

## 🌐 Expected API Endpoints

```
Auth      POST /api/auth/login     POST /api/auth/register
Students  CRUD /api/students             /{id}/tasks  /sales  /sessions
Mentors   CRUD /api/mentors              /{id}/batches /earnings /sessions
Admin     CRUD /api/admin/batches | students | teachers | earnings | feedback
Common    /api/leaderboard   /api/tasks   /api/sessions
```

> Responses should mirror the shapes currently hard‑coded in mock data.

---

## 🛠️ Getting Started

```bash
# 1. Clone
git clone https://github.com/<your‑org>/oll-bootcamp-frontend.git
cd oll-bootcamp-frontend

# 2. Install deps
npm install

# 3. Run dev server
npm run dev
```

The app expects the backend API to be accessible at **`http://localhost:3000`** by default (configure in `src/lib/api.ts`).

---

## 🧪 Tests

- Unit: Jest + React Testing Library for isolated components  
- Integration: role‑based flows & TanStack Query hooks  

---

## 🤝 Contributing

1. Create a feature branch  
2. Commit with conventional messages (e.g., `feat: add session attendance`)  
3. Create a PR against **main**  

Run `npm run lint && npm run format` before pushing.

---

## 📄 License

Distributed under the **MIT** license. See `LICENSE` for details.
