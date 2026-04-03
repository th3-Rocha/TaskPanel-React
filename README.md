# TaskPanel-React (Super Task Panel)

A task panel built with **React + Next.js (App Router)** to practice and study React concepts while building a small real-world UI.

Tasks are organized by priority:
- Urgent ⚡
- High 🔴
- Medium 🟡
- Low 🟢

## Backend (for studying React)

This project uses a **simple backend / mock API** only to **study React** with CRUD operations (create, read, update, delete).

The frontend communicates with the backend via HTTP requests using:

- `NEXT_PUBLIC_MOCK_API_SECRET` (base URL used by the fetch calls)
- Endpoints such as:
  - `POST /users` (create a user using Google `sub`)
  - `GET /users?sub=...` (find a user)
  - `GET /users/:id/tasks` (list tasks)
  - `POST /users/:id/tasks` (create a task)
  - `PUT /users/:id/tasks/:taskId` (edit a task)
  - `DELETE /users/:id/tasks/:taskId` (remove a task)

So: **the backend is not the main focus** — it exists only to support learning React by persisting tasks.

## Features

- Google Login (OAuth) using `@react-oauth/google`
- Protected tasks page (redirects to `/` if the token is missing/invalid)
- Task CRUD via mock backend
- Sorting tasks by:
  - Priority (descending) OR
  - Checked status
- Styled with Tailwind CSS

## Tech Stack

- **Next.js** (App Router)
- **React**
- **TypeScript**
- **Tailwind CSS**
- Google OAuth (`@react-oauth/google`)

## Getting Started

### 1) Install dependencies
```bash
npm install
```

### 2) Configure environment variables

Create a `.env.local` file in the project root:

```env
GOOGLE_CLIENT_ID=your_google_oauth_client_id
NEXT_PUBLIC_MOCK_API_SECRET=https://your-mock-api-url
```

**Notes**
- `GOOGLE_CLIENT_ID` is required by the Google OAuth Provider.
- `NEXT_PUBLIC_MOCK_API_SECRET` must be a reachable API base URL (mock server, json-server, etc.).

### 3) Run the project
```bash
npm run dev
```

Then open:
- http://localhost:3000

## Pages

- `/` → Login page
- `/tasks` → Task panel (requires a Google access token stored in `sessionStorage`)

## Project Goal

This repository is mainly for **studying React**:
- component composition
- state and effects
- client-side navigation
- API integration (fetch + async flows)
- UI behavior (modals, editing, sorting)

---

Made for learning and experimentation.
