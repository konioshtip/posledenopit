🚀 Solana DeFi Platform v2

A production-grade decentralized finance platform built on Solana, featuring AI-powered trading insights, real-time portfolio tracking, and seamless token swapping through Jupiter Protocol.
✨ Features

    🔄 Token Swapping: Powered by Jupiter Protocol for best execution

    💰 Portfolio Tracking: Real-time balance and performance analytics

    🤖 AI Trading Assistant: Powered by Deepseek AI for market insights

    📊 Price Charts: Historical price data and market trends

    🔒 Secure: Non-custodial, connect any Solana wallet

    ⚡ Fast: Built with Next.js and TypeScript for optimal performance

🚀 Quick Start
One-Command Start (Recommended)

# For development (hot reload)
npm run dev:quick

# For production testing  
npm run start:app

# To stop all services
npm run stop:app

Manual Setup

# 1. Install dependencies
npm run setup

# 2. Start development
npm run dev:quick

📖 Available Scripts
Command	Description	Use Case
npm run dev:quick	Quick development start with hot reload	Daily development
npm run start:app	Production build and start	Testing/deployment
npm run stop:app	Stop all services cleanly	Shutdown
npm run setup	Install dependencies and setup env	First time setup
npm run build	Build both services	CI/CD
npm run test	Run all tests	Quality assurance
npm run health	Check service health	Monitoring
npm run logs:backend	View backend logs	Debugging
npm run logs:frontend	View frontend logs	Debugging
🏗️ Architecture

┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │    Backend      │    │   Solana RPC    │
│   (Next.js)     │◄──►│   (Express)     │◄──►│   & Jupiter     │
│   Port: 3000    │    │   Port: 3001    │    │   Protocol      │
└─────────────────┘    └─────────────────┘    └─────────────────┘

Frontend (Next.js)

    Modern React with TypeScript

    Tailwind CSS for styling

    Wallet adapter integration

    Real-time data updates

Backend (Express + TypeScript)

    RESTful API design

    Real-time Solana data

    Jupiter Protocol integration

    AI-powered analytics

🔧 Configuration
Environment Variables

Backend (.env):

NODE_ENV=development
PORT=3001
SOLANA_RPC_URL=https://api.mainnet-beta.solana.com
SOLANA_NETWORK=mainnet-beta
DEEPSEEK_API_KEY=your_api_key_here  # Optional for AI features
CORS_ORIGIN=http://localhost:3000

Frontend (.env.local):

NEXT_PUBLIC_API_URL=http://localhost:3001
NEXT_PUBLIC_SOLANA_NETWORK=mainnet-beta

📊 API Endpoints
Health & Status

    GET /health - Service health check

    GET /api/monitoring/dashboard - System status

Token Operations

    GET /api/tokens/popular - Popular tokens

    GET /api/tokens/search?q={query} - Search tokens

    GET /api/tokens/{address} - Token details

Swap Operations

    GET /api/swap/quote - Get swap quote

    POST /api/swap/transaction - Create swap transaction

    POST /api/swap/send - Submit transaction

Portfolio Management

    GET /api/portfolio/balances?address={wallet} - Get balances

    GET /api/portfolio/analytics?address={wallet} - Portfolio analytics

🧪 Testing

# Run all tests
npm run test

# Backend tests only
npm run test:backend

# Frontend tests only  
npm run test:frontend

# Test API endpoints
npm run test:api

🔍 Monitoring & Debugging
Real-time Logs

# Backend logs
npm run logs:backend

# Frontend logs
npm run logs:frontend

Health Checks

# Check all services
npm run health

# Manual checks
curl http://localhost:3001/health
curl http://localhost:3000

Performance Monitoring

    Backend health dashboard: http://localhost:3001/api/monitoring/dashboard

    Real-time metrics and error tracking

    Circuit breaker status monitoring

🚀 Deployment
Production Build

# Build everything
npm run build

# Start production services
npm run start:app

Docker Deployment

# Build backend image
cd backend && docker build -t solana-defi-backend .

# Build frontend image  
cd frontend && docker build -t solana-defi-frontend .

# Start with docker-compose
docker-compose -f docker-compose.production.yml up

🛠️ Development
Project Structure

solana-defi-platform-v2/
├── 📂 backend/          # Express API server
│   ├── src/
│   │   ├── api/         # API routes
│   │   ├── services/    # Business logic
│   │   ├── utils/       # Utilities
│   │   └── types/       # TypeScript types
│   └── dist/            # Built files
├── 📂 frontend/         # Next.js application  
│   ├── app/             # App router pages
│   ├── components/      # React components
│   ├── lib/             # Utilities & hooks
│   └── .next/           # Built files
├── 📂 shared/           # Shared types
├── 🚀 start-app.sh      # Production start
├── 🛑 stop-app.sh       # Stop services
└── ⚡ dev-start.sh      # Development start

Development Workflow

    Start Development: npm run dev:quick

    Make Changes: Hot reload active for both services

    Test: Changes reflected immediately

    Build: npm run build when ready

    Deploy: npm run start:app for production testing

🔒 Security

    Non-custodial: No private keys stored

    Input validation: All API inputs validated

    Rate limiting: Protection against abuse

    CORS protection: Secure cross-origin requests

    Error sanitization: No sensitive data in responses

📱 Wallet Support

    Phantom (Recommended)

    Solflare

    Ledger

    Torus

    Standard Wallet (Auto-detected)

🤝 Contributing

    Fork the repository

    Create a feature branch

    Make your changes

    Add tests

    Submit a pull request

📄 License

MIT License - see LICENSE file for details.
🆘 Support
Troubleshooting

Port conflicts?

npm run stop:app && npm run dev:quick

Dependencies issues?

npm run clean && npm run setup

Environment problems?

npm run setup:env

Getting Help

    Check the Quick Start Guide

    Review logs: npm run logs:backend or npm run logs:frontend

    Check health: npm run health

    Join our Discord (coming soon)

Built with ❤️ for the Solana ecosystem
