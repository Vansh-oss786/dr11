# 🚀 CricketFan11 Deployment Instructions

## Quick Deployment on Replit

### Option 1: Fork This Repl
1. **Fork this Repl** from the current workspace
2. **Set Environment Variables** in your forked Repl:
   ```
   DATABASE_URL=your_postgresql_connection_string
   JWT_SECRET=your_secret_key_here
   ```
3. **Run Database Setup**:
   ```bash
   npm run db:push
   ```
4. **Start the Application**:
   ```bash
   npm run dev
   ```

### Option 2: Deploy to Replit from GitHub
1. **Create new Repl** and import from GitHub
2. **Install dependencies**: `npm install`
3. **Configure environment variables**
4. **Setup database and run**

## 📦 Download & Local Setup

### Prerequisites
- Node.js 18+
- PostgreSQL database
- Git

### Download Options

#### Option 1: Download ZIP from Replit
1. Click the three dots menu in Replit
2. Select "Download as ZIP"
3. Extract the downloaded file
4. Follow local setup instructions below

#### Option 2: Clone from GitHub
```bash
git clone https://github.com/your-username/cricketfan11
cd cricketfan11
```

### Local Development Setup

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Environment Configuration**
   Create `.env` file:
   ```env
   DATABASE_URL=postgresql://username:password@localhost:5432/cricketfan11
   JWT_SECRET=your-super-secret-jwt-key-here
   NODE_ENV=development
   ```

3. **Database Setup**
   ```bash
   # Push schema to database
   npm run db:push
   
   # The database will be populated with sample data automatically
   ```

4. **Start Development Server**
   ```bash
   npm run dev
   ```

5. **Access the Application**
   - Frontend: http://localhost:5000
   - API: http://localhost:5000/api

### Test the Application
Use these credentials to test:
- **User**: `player@cricketfan11.com` / `player123`
- **Admin**: `admin@cricketfan11.com` / `admin123`

## 🌐 Production Deployment

### Deploy to Vercel
1. **Install Vercel CLI**:
   ```bash
   npm i -g vercel
   ```

2. **Deploy**:
   ```bash
   vercel --prod
   ```

3. **Set Environment Variables** in Vercel dashboard

### Deploy to Railway
1. **Connect GitHub repo** to Railway
2. **Set environment variables**
3. **Deploy automatically** on push

### Deploy to Heroku
1. **Create Heroku app**:
   ```bash
   heroku create cricketfan11-app
   ```

2. **Set environment variables**:
   ```bash
   heroku config:set DATABASE_URL=your_db_url
   heroku config:set JWT_SECRET=your_secret
   ```

3. **Deploy**:
   ```bash
   git push heroku main
   ```

## 🔧 Configuration Guide

### Database Configuration

#### PostgreSQL Setup
```bash
# Install PostgreSQL locally
sudo apt-get install postgresql postgresql-contrib

# Create database
sudo -u postgres createdb cricketfan11

# Create user
sudo -u postgres createuser --interactive
```

#### Using Neon (Recommended)
1. Create account at https://neon.tech
2. Create new database
3. Copy connection string to `DATABASE_URL`

### Environment Variables Reference
```env
# Required
DATABASE_URL=postgresql://...
JWT_SECRET=your-secret-key

# Optional
NODE_ENV=production
PORT=5000
REPLIT_DOMAINS=your-domain.replit.app

# Future integrations
PAYMENT_GATEWAY_KEY=your-razorpay-key
EMAIL_SERVICE_KEY=your-email-key
CRICKET_API_KEY=your-cricket-api-key
```

## 📱 Mobile & PWA Setup

### Enable PWA Features
1. **Add to manifest.json**:
   ```json
   {
     "name": "CricketFan11",
     "short_name": "CricketFan11",
     "start_url": "/",
     "display": "standalone",
     "theme_color": "#0f766e",
     "background_color": "#ffffff"
   }
   ```

2. **Add service worker** for offline support

### Mobile Optimization
- Already responsive with mobile-first design
- Touch-friendly interface
- Optimized for mobile cricket fans

## 🛠️ Troubleshooting

### Common Issues

#### Database Connection Error
```bash
# Check DATABASE_URL format
DATABASE_URL=postgresql://user:pass@host:port/database

# Test connection
npm run db:push
```

#### JWT Authentication Issues
```bash
# Ensure JWT_SECRET is set
echo $JWT_SECRET

# Clear browser storage if needed
localStorage.clear()
```

#### Port Already in Use
```bash
# Kill process on port 5000
lsof -ti:5000 | xargs kill -9

# Or use different port
PORT=3000 npm run dev
```

### Getting Help
1. **Check logs** in Replit console
2. **Review network requests** in browser dev tools
3. **Check database** connection and schema
4. **Verify environment** variables are set

## 📊 Monitoring & Analytics

### Add Monitoring (Optional)
```javascript
// Add to client/src/main.tsx
import { analytics } from './lib/analytics';

// Track user interactions
analytics.track('team_created', { match_id, players_count });
```

### Performance Monitoring
- Use browser dev tools
- Monitor database query performance
- Check API response times

This deployment guide ensures you can get CricketFan11 running in any environment quickly and efficiently!