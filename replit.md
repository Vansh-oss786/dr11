# CricketFan11 - Fantasy Cricket Platform

## Overview

CricketFan11 is a comprehensive fantasy cricket platform built with a modern full-stack architecture. The application allows users to create fantasy teams, participate in contests, manage their wallets, and compete for prizes based on real cricket match performances. The platform includes both user and admin portals with complete functionality for fantasy sports management.

## Recent Changes (January 2025)

✅ **Authentication System Fully Fixed** (January 26, 2025)
- Resolved login/registration field mapping issues (fullName vs username)
- Fixed backend authentication middleware TypeScript errors
- Added missing type declarations for bcrypt and jsonwebtoken
- Synchronized token storage between login page and auth service
- Verified both user and admin login endpoints working correctly
- Registration system creates new users successfully

✅ **Complete Documentation Package Created**
- Added comprehensive README.md with setup instructions
- Created DEVELOPMENT_GUIDE.md with 8-week implementation roadmap
- Added DEPLOYMENT_INSTRUCTIONS.md for production deployment
- Generated DOWNLOAD_GUIDE.md for easy package distribution
- Documented all remaining features and implementation steps

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Library**: Shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom cricket-themed color palette
- **State Management**: TanStack React Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Database**: PostgreSQL (configured for Neon serverless)
- **Authentication**: JWT-based authentication with bcrypt password hashing
- **Session Management**: Express sessions with PostgreSQL store

### Database Architecture
- **Primary Database**: PostgreSQL with comprehensive schema design
- **ORM**: Drizzle ORM with schema validation using Zod
- **Migration System**: Drizzle Kit for database migrations
- **Connection**: Neon serverless PostgreSQL with connection pooling

## Key Components

### Authentication & Authorization
- JWT-based authentication system
- Role-based access control (player/admin)
- Secure password hashing with bcrypt
- Test credentials for development:
  - User: `player@cricketfan11.com` / `player123`
  - Admin: `admin@cricketfan11.com` / `admin123`

### User Management System
- Complete user registration and profile management
- KYC status tracking (pending/verified/rejected)
- Wallet management with separate tracking for deposits and winnings
- Referral system support

### Fantasy Sports Core
- **Team Builder**: Advanced team creation with position constraints
  - 11 players total with specific position limits
  - Credit system for balanced team selection
  - Captain/Vice-Captain selection with point multipliers
- **Contest Management**: Multiple contest types with varying entry fees
- **Scoring System**: Comprehensive point calculation based on player performance
- **Leaderboard**: Real-time contest rankings and prize distribution

### Financial System
- Integrated wallet management
- Transaction tracking for deposits, withdrawals, and contest fees
- Prize distribution system
- Support for multiple payment methods (UPI, bank transfers)

### Admin Portal
- Complete administrative dashboard
- Match and contest management
- User management and KYC verification
- Financial oversight and reporting
- Player performance tracking

## Data Flow

### User Registration & Authentication Flow
1. User registers with email/phone verification
2. JWT token issued upon successful authentication
3. Token stored in localStorage for session persistence
4. Protected routes validate token on each request

### Fantasy Team Creation Flow
1. User selects a live/upcoming match
2. System fetches available players with credits and positions
3. User builds team within constraints (11 players, position limits)
4. Team validation ensures credit limits and position requirements
5. Captain/Vice-Captain selection for point multipliers

### Contest Participation Flow
1. User joins contest with entry fee deduction from wallet
2. Team submission locks lineup before match start
3. Real-time scoring updates during match
4. Prize distribution based on final leaderboard positions

### Wallet Management Flow
1. Secure deposit processing through payment gateways
2. Transaction logging for all financial activities
3. Automatic prize credit for winning positions
4. Withdrawal processing with verification

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL database connectivity
- **drizzle-orm**: Type-safe database operations
- **@tanstack/react-query**: Server state management
- **@radix-ui/react-***: UI component primitives
- **bcrypt**: Password hashing
- **jsonwebtoken**: JWT authentication
- **zod**: Schema validation

### Development Dependencies
- **vite**: Build tool and development server
- **typescript**: Type checking
- **tailwindcss**: Utility-first CSS framework
- **drizzle-kit**: Database migration tool

### UI Component System
- Comprehensive Shadcn/ui component library
- Cricket-themed design system with green and gold colors
- Responsive design with mobile-first approach
- Accessible components built on Radix UI

## Deployment Strategy

### Development Environment
- Vite development server with HMR
- Replit integration with runtime error overlay
- Environment-specific configuration
- Database migrations through Drizzle Kit

### Production Build Process
1. Frontend build using Vite with optimized assets
2. Backend compilation using esbuild for Node.js
3. Static assets served from Express
4. Database schema deployment via migrations

### Environment Configuration
- Database URL configuration for Neon PostgreSQL
- JWT secret management
- Environment-specific feature flags
- Replit-specific development tools integration

### Database Management
- Automated schema migrations
- Connection pooling for production scalability
- Backup and recovery procedures
- Performance monitoring and optimization

The application is designed to handle the complete fantasy cricket experience from user registration to prize distribution, with a focus on real-time updates, secure financial transactions, and comprehensive administrative controls.