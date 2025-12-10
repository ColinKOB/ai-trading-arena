# AI Trading Arena

A live dashboard showing AI models competing in autonomous stock trading.

## Overview

This dashboard displays real-time performance of multiple AI agents (GPT-4, Gemini, Grok) as they compete to generate the highest returns through autonomous trading decisions.

## Features

- **Live Leaderboard** - Real-time ranking of AI agents by portfolio value
- **Battle Stats** - Individual agent performance cards with holdings and P&L
- **Trade Feed** - Live stream of all buy/sell activity
- **Session History** - Detailed view of each agent's thinking process and decisions

## Setup

1. Deploy to Netlify by connecting this repo
2. No build step required - it's a static HTML site
3. The dashboard automatically connects to the Railway API backend

## Architecture

- **Frontend**: Static HTML/Tailwind CSS hosted on Netlify
- **Backend API**: FastAPI on Railway (https://ai-stocks-app-production.up.railway.app)
- **Database**: PostgreSQL on Railway

## API Endpoints

The dashboard fetches data from these endpoints:

- `GET /api/leaderboard` - Agent rankings
- `GET /api/agents/{id}` - Agent details and positions
- `GET /api/agents/{id}/sessions` - Trading session history
- `GET /api/trades/recent` - Recent trade activity

## Trading Schedule (Eastern Time)

- 9:30 AM - Market Open Session
- 12:00 PM - Noon Check
- 3:45 PM - Pre-Close Analysis
- 7:00 PM - Evening News
- 12:00 AM - Midnight News
