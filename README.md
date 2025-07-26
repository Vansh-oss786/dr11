# CricketFan11 - Fantasy Cricket Platform

A comprehensive fantasy cricket platform built with modern web technologies, featuring team creation, contests, live scoring, and administrative controls.

## 🏏 What This Platform Offers

### Core Fantasy Cricket Features
- **Team Builder**: Create fantasy teams with position constraints (1-8 players per position)
- **Captain/Vice-Captain**: Select multipliers for extra points (2x for captain, 1.5x for vice-captain)
- **Multiple Teams**: Create up to 11 teams per match
- **Contest System**: Join contests with entry fees and prize pools
- **Live Scoring**: Real-time player performance tracking
- **Leaderboards**: Contest rankings and prize distribution

### User Management
- **Authentication**: Secure login/registration system
- **Wallet Management**: Deposit, withdraw, and track balance
- **KYC Verification**: Document verification system
- **Referral System**: Earn rewards for referring friends
- **Transaction History**: Complete financial tracking

### Admin Portal
- **Match Management**: Create and manage cricket matches
- **Contest Control**: Set up contests with prizes
- **User Management**: Handle user accounts and KYC
- **Financial Oversight**: Monitor transactions and payouts
- **Player Database**: Maintain player profiles and statistics

## 🚀 Technology Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development
- **Tailwind CSS** with custom cricket theme
- **Shadcn/ui** components
- **TanStack React Query** for state management
- **Wouter** for routing

### Backend
- **Node.js** with Express
- **TypeScript** with ES modules
- **Drizzle ORM** for database operations
- **JWT Authentication** with bcrypt
- **PostgreSQL** database

## 📦 Installation & Setup

### Prerequisites
- Node.js 18+ 
- PostgreSQL database
- Git

### Quick Start
1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd cricketfan11
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env` file:
   ```env
   DATABASE_URL=your_postgresql_connection_string
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   ```

4. **Database Setup**
   ```bash
   npm run db:push
   ```

5. **Start Development Server**
   ```bash
   npm run dev
   ```

The application will be available at `http://localhost:5000`

### Test Credentials
- **User Account**: `player@cricketfan11.com` / `player123`
- **Admin Account**: `admin@cricketfan11.com` / `admin123`

## 🏗️ Project Structure

```
cricketfan11/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Application pages
│   │   ├── hooks/         # Custom React hooks
│   │   └── lib/           # Utilities and services
├── server/                # Backend Express application
│   ├── db.ts             # Database connection
│   ├── routes.ts         # API endpoints
│   └── storage.ts        # Data access layer
├── shared/               # Shared types and schemas
│   └── schema.ts         # Database schema definitions
└── scripts/              # Utility scripts
```

## 🎯 Current Status

### ✅ Completed Features
- Modern Dream11-inspired UI with teal-purple gradients
- Complete authentication system (login/register/JWT)
- User and Admin dashboards with analytics
- Team builder with position constraints
- Database schema with sample data
- Responsive mobile-first design

### 🚧 Remaining Work to Complete

#### Phase 1: Core Fantasy Features (High Priority)
1. **Multiple Team Creation**
   - Allow users to create up to 11 teams per match
   - Team management interface
   - Bulk team operations

2. **Contest System Enhancement**
   - Contest filtering and search
   - Entry fee payment integration
   - Prize pool calculations
   - Contest joining logic

3. **Live Scoring System**
   - Real-time player point updates
   - Match status tracking
   - Automatic score calculations

#### Phase 2: Financial Integration (Medium Priority)
4. **Payment Gateway Integration**
   - UPI payment processing
   - Bank transfer support
   - Withdrawal system
   - Transaction verification

5. **Wallet System Enhancement**
   - Separate deposit/winnings tracking
   - Withdrawal limits and rules
   - Bonus credit management

#### Phase 3: Advanced Features (Medium Priority)
6. **Leaderboard System**
   - Real-time contest rankings
   - Prize distribution logic
   - Winner announcements
   - Historical performance

7. **KYC Verification**
   - Document upload system
   - Admin verification workflow
   - Status tracking and notifications

#### Phase 4: User Engagement (Low Priority)
8. **Referral System**
   - Referral code generation
   - Reward tracking
   - Bonus distribution

9. **Notifications System**
   - Real-time updates
   - Email notifications
   - Push notifications

10. **Mobile App Optimization**
    - PWA implementation
    - Mobile-specific features
    - Offline capabilities

## 🛠️ Development Guidelines

### Adding New Features
1. **Database Changes**: Update `shared/schema.ts` first
2. **Backend**: Add routes in `server/routes.ts`
3. **Storage**: Implement data operations in `server/storage.ts`
4. **Frontend**: Create components and pages
5. **Testing**: Test with sample data

### Code Standards
- Use TypeScript for type safety
- Follow existing component patterns
- Implement proper error handling
- Add loading states for async operations

### Database Operations
- Use Drizzle ORM for all database operations
- Run `npm run db:push` after schema changes
- Never write raw SQL migrations

## 📱 Screenshots & Demo

The platform features a modern, mobile-first design with:
- Clean authentication flows
- Intuitive team building interface
- Comprehensive admin controls
- Real-time data updates
- Responsive design across devices

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Implement changes with tests
4. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🔗 Links

- **Live Demo**: [Deploy on Replit]
- **Documentation**: See this README
- **Issues**: GitHub Issues page
- **Support**: Contact development team

---

**Note**: This is a comprehensive fantasy sports platform. Ensure compliance with local gambling and fantasy sports regulations before deployment.