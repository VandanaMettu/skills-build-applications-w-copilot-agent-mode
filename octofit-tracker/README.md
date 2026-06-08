# OctoFit Tracker

A modern multi-tier application for fitness tracking built with React 19 (frontend) and Express + Node.js (backend), with MongoDB for data persistence.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite application
│   ├── src/
│   ├── package.json
│   └── vite.config.js
└── backend/           # Express + TypeScript backend
    ├── src/
    │   └── server.ts
    ├── package.json
    ├── tsconfig.json
    └── .env
```

## Tech Stack

### Frontend
- **React 19.2.6** - Latest React with modern features
- **Vite 8.0.12** - Fast build tool and dev server
- **ESLint** - Code quality and linting
- **Port:** 5173

### Backend
- **Express 5.2.1** - Web framework for Node.js
- **TypeScript 6.0.3** - Type-safe JavaScript
- **Mongoose 9.6.3** - MongoDB ODM for data access
- **ts-node** - Execute TypeScript directly
- **Port:** 8000

### Database
- **MongoDB** - NoSQL database
- **Port:** 27017
- **Database URI:** `mongodb://localhost:27017/octofit`

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm (v11 or higher)
- MongoDB (running locally or via Docker)

### Frontend Setup

```bash
cd octofit-tracker/frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`

### Backend Setup

```bash
cd octofit-tracker/backend
npm install
npm run dev
```

The backend API will be available at `http://localhost:8000`

**Health Check Endpoint:** `GET /api/health`

### Running MongoDB

If you don't have MongoDB running locally, you can start it using Docker:

```bash
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

## Available Scripts

### Frontend
- `npm run dev` - Start development server with Vite
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

### Backend
- `npm run dev` - Start development server with ts-node
- `npm run build` - Compile TypeScript to JavaScript
- `npm run start` - Run compiled JavaScript
- `npm test` - Run tests

## Configuration

### Backend Environment Variables

Create a `.env` file in the `octofit-tracker/backend` directory:

```env
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit
NODE_ENV=development
```

## API Endpoints

### Health Check
- `GET /api/health` - Returns server status and timestamp

More endpoints will be added as features are developed.

## Development Workflow

1. Start MongoDB
2. Run backend: `cd backend && npm run dev`
3. Run frontend in another terminal: `cd frontend && npm run dev`
4. Open `http://localhost:5173` in your browser
5. The frontend will communicate with the backend at `http://localhost:8000`

## Next Steps

- [ ] Create React components for the UI
- [ ] Define MongoDB schemas and models
- [ ] Build API endpoints for fitness tracking
- [ ] Implement authentication
- [ ] Add data validation
- [ ] Deploy to production
