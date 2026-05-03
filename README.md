# 💰 Cash Me If You Can 

A modern, AI-powered trivia game built with Next.js and Firebase. Test your knowledge, compete with others, and use intelligent lifelines to climb the leaderboard!

## ✨ Features

- **Interactive Trivia Gameplay**: Engaging questions with multiple-choice answers and real-time feedback
- **Countdown Timer**: Adds urgency and excitement to each question
- **AI Phone-A-Friend Lifeline**: Get assistance from an AI-powered advisor that mimics human intuition
- **Dynamic Scoring System**: Points awarded based on question difficulty
- **Global Leaderboard**: Compete with other players and track your ranking
- **User Authentication**: Secure sign-up and sign-in with Firebase
- **Responsive Design**: Beautiful UI with smooth animations and transitions
- **Modern UI Components**: Built with Radix UI and Tailwind CSS

## 🚀 Tech Stack

- **Frontend Framework**: Next.js 15.2.3 with Turbopack
- **Language**: TypeScript
- **Styling**: Tailwind CSS with custom animations
- **UI Components**: Radix UI
- **Backend/Database**: Firebase (Authentication & Firestore)
- **AI Integration**: Google Genkit for AI-powered flows
- **State Management**: React Query with Firebase integration
- **Form Handling**: React Hook Form with Zod validation
- **Icons**: Lucide React
- **Charts**: Recharts for data visualization

## 📋 Prerequisites

- Node.js 18+ and npm 11+
- Firebase project (with authentication and Firestore enabled)
- Google API credentials for Genkit AI
- Git

## 🛠️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/gaurav-gehlot1/cash_me_if_u_can.git
cd CMIUCAN-DEPLOYMENT-main
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment Variables
Create a `.env.local` file in the project root with your Firebase and AI configuration:

```env
# Firebase Configuration
NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

# Google Genkit Configuration
GOOGLE_GENKIT_API_KEY=your_genkit_api_key
```

### 4. Run Development Server
```bash
npm run dev
```

The application will be available at `http://localhost:9002`

## 📁 Project Structure

```
src/
├── ai/                          # AI/Genkit flows
│   ├── genkit.ts               # Main Genkit configuration
│   ├── dev.ts                  # Development setup
│   └── flows/
│       ├── generate-trivia-questions-flow.ts  # Question generation
│       └── phone-a-friend.ts   # AI lifeline implementation
├── app/                        # Next.js app router
│   ├── page.tsx               # Home page
│   ├── layout.tsx             # Root layout
│   ├── globals.css            # Global styles
│   ├── auth/
│   │   ├── signin/page.tsx    # Sign-in page
│   │   └── signup/page.tsx    # Sign-up page
│   ├── play/page.tsx          # Game play page
│   └── leaderboard/page.tsx   # Leaderboard page
├── components/                # React components
│   ├── game/                  # Game-specific components
│   │   ├── GameArea.tsx
│   │   ├── QuestionDisplay.tsx
│   │   ├── AnswerOption.tsx
│   │   ├── TimerDisplay.tsx
│   │   ├── ScoreDisplay.tsx
│   │   ├── LifelinePanel.tsx
│   │   ├── PhoneAFriendDialog.tsx
│   │   ├── AudiencePollDialog.tsx
│   │   └── GameOverDialog.tsx
│   ├── layout/                # Layout components
│   │   ├── Header.tsx
│   │   └── Footer.tsx
│   └── ui/                    # Reusable UI components
├── hooks/                     # Custom React hooks
│   ├── use-game-state.ts     # Game state management
│   ├── use-timer.ts          # Timer hook
│   ├── use-toast.ts          # Toast notifications
│   └── use-mobile.tsx        # Mobile detection
├── context/                   # React context
│   └── AuthContext.tsx        # Authentication context
└── lib/                       # Utilities and configuration
    ├── firebase/config.ts     # Firebase initialization
    ├── types.ts               # TypeScript types
    ├── game-data.ts           # Game data and constants
    └── utils.ts               # Utility functions
```

## 📝 Available Scripts

- `npm run dev` - Start development server on port 9002
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint
- `npm run typecheck` - Run TypeScript type checking
- `npm run genkit:dev` - Start Genkit development server
- `npm run genkit:watch` - Start Genkit with file watch mode

## 🎮 Game Flow

1. **Home Page** (`/`) - Select game options and difficulty level
2. **Game Page** (`/play`) - Answer trivia questions within the time limit
3. **Lifelines** - Use "Phone-A-Friend" or "Audience Poll" to get assistance
4. **Scoring** - Points awarded based on difficulty and speed
5. **Leaderboard** (`/leaderboard`) - View global rankings and your score

## 🔐 Authentication

The application uses Firebase Authentication with support for:
- Email/Password sign-up and sign-in
- User profile management
- Session persistence

## 🤖 AI Integration

**Phone-A-Friend Lifeline**: Powered by Google Genkit, providing AI-assisted answers with controlled uncertainty to simulate human-like advice.

## 🎨 Design System

- **Primary Color**: Vivid Purple (#9400D3)
- **Background**: Soft Lavender (#E6E6FA)
- **Accent Color**: Electric Indigo (#6F00FF)
- **Typography**: Clean, readable fonts optimized for gaming experience
- **Animations**: Subtle transitions for enhanced UX

## 📱 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🐛 Bug Reports & Suggestions

Please open an issue on the [GitHub repository](https://github.com/gaurav-gehlot1/cash_me_if_u_can/issues) to report bugs or suggest features.

## 📄 License

This project is private. All rights reserved.

## 👤 Author

**Gaurav Gehlot**
- GitHub: [@gaurav-gehlot1](https://github.com/gaurav-gehlot1)

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- UI Components from [Radix UI](https://www.radix-ui.com/)
- Styling with [Tailwind CSS](https://tailwindcss.com/)
- AI powered by [Google Genkit](https://github.com/firebase/genkit)
- Backend by [Firebase](https://firebase.google.com/)

---

**Made with ❤️ for trivia enthusiasts everywhere!**
