**This project is a part of a hackathon run by https://www.katomaran.com**

**ARCHITECTURE DIAGRAM**
┌─────────────────────────────────────────────┐
│                Frontend (Expo App)          │
│                                             │
│  - React Native UI                          │
│  - Expo Router for navigation               │
│  - Google OAuth Login (expo-auth-session)   │
│  - Task List UI, Animations, FAB etc.       │
│                                             │
│         ▲              |                    │
│         │  Axios REST  |                    │
│         │  API Calls   ▼                    │
└─────────┼──────────────┼────────────────────┘
          │              │
          │              │
┌─────────▼──────────────▼──────────────┐
│            Node.js / Express API      │
│                                        │
│ - Routes:                              │
│    • GET    /api/todos                 │
│    • POST   /api/todos                 │
│    • PUT    /api/todos/:id             │
│    • DELETE /api/todos/:id             │
│                                        │
│ - All data stored in a shared in-memory│
│   array accessible to all users        │
│                                        │
│ - No database involved                 │
└─────────┬──────────────┬───────────────┘
          │              │
          │              │
          │              │
      ┌───▼──────────────▼───────────┐
      │      External Services      │
      │                             │
      │ - Google OAuth2 Provider    │
      │   • Handles login, tokens   │
      │                             │
      └─────────────────────────────┘
      
VIDEO LINK:https://drive.google.com/file/d/1dW2S98of4Ao-lN8EV4TNA5Zi9LUy1R1x/view?usp=sharing
