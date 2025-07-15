// Project: RehabConnect - Patient Progress Tracker
// Frontend: React

# RehabConnect Frontend – React

A frontend web application for patients to log physical therapy sessions and for PTs to view and manage rehab progress. This version uses React and is designed to connect with any of the RehabConnect backend APIs (PostgreSQL, DynamoDB, MongoDB).

---

## Features
- Patient login and secure access (integrated with Cognito or other auth)
- Log daily rehab activities
- View progress history and pain level trends
- Connects to RESTful API

---

## Tech Stack
- React (with Hooks)
- Axios (API calls)
- React Router DOM
- CSS Modules / Tailwind / Styled Components (optional styling)
- Deployed via Vercel / Netlify / S3

---

## Folder Structure
```
rehabconnect-frontend/
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/ (API functions)
│   └── App.js
├── .env
├── package.json
└── README.md
```

---

## Setup Instructions
```bash
git clone https://github.com/yourusername/rehabconnect-frontend.git
cd rehabconnect-frontend
npm install
npm start
```

Update `.env` with your backend API URL:
```
REACT_APP_API_BASE_URL=https://your-api-url.com
```

---

## Pages
- `/login` – User login page (Cognito/Auth placeholder)
- `/log` – Submit new rehab session
- `/progress/:patientId` – View progress log
- `/plan` – Rehab plan overview (if PT)

---

## Coming Soon
- Charts & graphs using Chart.js or Recharts
- Auth token handling with AWS Cognito
- Mobile responsive design

---

## Architecture Overview
```
[React Frontend]
      ↓
[REST API: /log, /progress]
      ↓
[Spring Boot / Node API Layer]
      ↓
[PostgreSQL / MongoDB / DynamoDB]
```

---

## Example Payload
```json
{
  "patientId": "abc-123",
  "painLevel": 3,
  "exercises": ["Bridge", "Bird Dog"],
  "repsCompleted": 25
}
```

---

## License
MIT

