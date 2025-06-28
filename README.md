# Poll Generation App

A full-stack application for creating and managing polls with AI-powered question generation capabilities.

## Project Structure

```
POLL_GENERATION_APP/
├── package.json                 # Root package.json for monorepo
├── pnpm-workspace.yaml         # PNPM workspace configuration
├── README.md                   # This file
├── backend/                    # Express.js TypeScript backend
│   ├── package.json
│   ├── tsconfig.json
│   ├── src/
│   │   ├── app.ts
│   │   ├── server.ts
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── types/
│   │   └── utils/
│   └── dist/                   # Compiled JavaScript files
└── frontend/                   # React TypeScript frontend
    ├── package.json
    ├── vite.config.ts
    ├── tsconfig.json
    ├── src/
    │   ├── App.tsx
    │   ├── main.tsx
    │   ├── components/
    │   ├── contexts/
    │   └── pages/
    └── dist/                   # Built frontend assets
```

## Prerequisites

- Node.js >= 18.0.0
- PNPM >= 8.0.0
- MongoDB Atlas account (for database)

## Installation

1. Clone the repository
2. Install dependencies for the entire project:
   ```bash
   pnpm install
   ```

## Development

### Start both frontend and backend in development mode:
```bash
pnpm dev
```

### Start backend only:
```bash
pnpm dev:backend
```

### Start frontend only:
```bash
pnpm dev:frontend
```

## Building

### Build both frontend and backend:
```bash
pnpm build
```

### Build backend only:
```bash
pnpm build:backend
```

### Build frontend only:
```bash
pnpm build:frontend
```

## Production

### Start the production server (backend):
```bash
pnpm start
```

## Environment Variables

Create a `.env` file in the `backend/` directory with the following variables:

```env
PORT=5000
MONGODB_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret_key
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
```

## Features

### Backend
- RESTful API with Express.js and TypeScript
- MongoDB Atlas integration with Mongoose
- JWT authentication
- Email notifications with Nodemailer
- CORS enabled for frontend communication
- Error handling middleware

### Frontend
- React with TypeScript and Vite
- Modern UI with Tailwind CSS
- Responsive design with Framer Motion animations
- Authentication system
- Poll creation and management
- Real-time updates
- Charts and data visualization with Recharts

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/forgot-password` - Forgot password
- `POST /api/auth/reset-password` - Reset password

### Polls
- `GET /api/polls` - Get all polls
- `POST /api/polls` - Create new poll
- `GET /api/polls/:id` - Get specific poll
- `PUT /api/polls/:id` - Update poll
- `DELETE /api/polls/:id` - Delete poll

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

### Reports
- `GET /api/reports` - Get reports
- `POST /api/reports` - Create report

## Technologies Used

### Backend
- Express.js
- TypeScript
- MongoDB Atlas
- Mongoose
- JWT
- Bcrypt.js
- Nodemailer
- CORS

### Frontend
- React 18
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- React Router DOM
- React Hook Form
- Recharts
- Lucide React

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and ensure builds pass
5. Submit a pull request

## License

MIT License
