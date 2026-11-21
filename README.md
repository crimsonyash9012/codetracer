# CodeTracer

A DSA practice platform with a code editor, C++ execution, AI hints, and algorithm visualizations.

## Features

- Practice coding problems and run solutions against test cases.
- Get AI guidance and visualize algorithms step by step.
- Join contests, view leaderboards, and track progress.
- Connect with friends through chat and notifications.

## Tech stack

React, Vite, TypeScript, Express, Socket.IO, PostgreSQL, Prisma, Judge0, and OpenAI.

## Local setup

Requires Node.js, npm, PostgreSQL, and credentials for Google OAuth, Judge0, and OpenAI.

```bash
git clone https://github.com/crimsonyash9012/codetracer.git
cd codetracer
npm install
cp packages/backend/.env.example packages/backend/.env
cp packages/frontend/.env.example packages/frontend/.env.local
```

Fill in the backend environment variables. For local development, use `http://localhost:5173` for `FRONTEND_URL` and `http://localhost:3001` for the frontend's `VITE_API_URL` and `VITE_SOCKET_URL`. Configure the Google OAuth callback to match your backend.

Export the same `DATABASE_URL` in your terminal, then initialize the database and start the app:

```bash
npm run prisma:generate -w @algoarena/backend
npm run prisma:migrate -w @algoarena/backend
npm run build -w @algoarena/shared
npm run dev
```

Frontend: http://localhost:5173. Backend: http://localhost:3001.

## Credits

Based on [tanishbajaj101/codetracer](https://github.com/tanishbajaj101/codetracer). Original commit history is preserved.
