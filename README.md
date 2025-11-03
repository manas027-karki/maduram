# Maduram | Jeevan-Amrit

A modern health and wellness web application designed to help users track their emotional wellbeing through mindful reflection and AI-powered mood analysis. Built with React, Zustand, and a beautiful, calming interface inspired by wellness and meditation principles.

## 🌟 Features

### Moodify
Express your feelings in three intuitive ways:
- **Text Input**: Write freely about your emotions and receive personalized insights
- **Voice Recording**: Record your thoughts and feelings through audio
- **Video Capture**: Capture your emotional state through video analysis

Each input generates a calming AI-style message tailored to your mood with actionable wellness suggestions.

### Feeling Tracker
Visualize and understand your emotional journey:
- **Weekly Wellness Trends**: Line chart showing your emotional wellbeing scores over 7 days
- **Mood Distribution**: Pie chart displaying the breakdown of your emotions
- **7-Day Summary**: Quick overview with dominant mood, total entries, and tracked days
- **Wellness Journal**: Reflective journaling space to document your thoughts and feelings

### Home Page
A serene landing experience featuring:
- Sanskrit shlokas with English translations
- Smooth animations and transitions
- Quick access to both Moodify and Feeling Tracker features
- Calming gradient design with teal and green tones

## 🛠️ Tech Stack

### Frontend
- **React** - UI library
- **TypeScript** - Type safety
- **Zustand** - State management
- **TailwindCSS** - Styling
- **Framer Motion** - Animations
- **Recharts** - Data visualization
- **Axios** - HTTP requests
- **Lucide React** - Icons

### Architecture
```
src/
├── api/
│   └── api.js                 # API endpoints configuration
├── components/
│   ├── Home.jsx               # Landing page with Sanskrit theme
│   ├── Moodify.jsx            # Mood input (text, voice, video)
│   └── FeelingTracker.jsx     # Charts and journaling dashboard
├── store/
│   ├── moodStore.js           # Mood state and analysis logic
│   └── trackerStore.js        # History and journal management
└── App.tsx                    # Main app with navigation
```

## 🚀 Getting Started

### Prerequisites
- Node.js 16+
- npm or yarn

### Installation

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file (optional, for backend connection):
```env
VITE_API_URL=http://localhost:5000/api
```

3. Start the development server:
```bash
npm run dev
```

4. Build for production:
```bash
npm run build
```

## 📊 How to Use

### Tracking Your Mood
1. From the home page, click **"Moodify"**
2. Choose your preferred input method (text, voice, or video)
3. Express your feelings
4. Receive personalized insights and suggestions

### Viewing Your Progress
1. From the home page, click **"Feeling Tracker"**
2. Navigate between tabs:
   - **Trends**: View your wellness scores over 7 days
   - **Distribution**: See the breakdown of your emotions
   - **Journal**: Add reflections and view past entries

## 🔌 API Endpoints (Ready for Backend Integration)

The application is configured to connect to these endpoints:

### Mood Analysis
- `POST /api/moodify/analyze` - Analyze mood from input (text, voice, or video)
- `POST /api/moodify/store` - Store analyzed mood to database

### Tracker
- `GET /api/tracker/get?userId={userId}&days={days}` - Fetch mood history
- `POST /api/tracker/journal` - Add journal entry
- `GET /api/tracker/journal?userId={userId}` - Fetch journal entries

**Note**: Currently, the app uses mock data when the backend is unavailable. Backend integration will replace these mock responses.

## 🧠 State Management with Zustand

### Mood Store (`src/store/moodStore.js`)
Manages current mood state and analysis:
- `analyzeMood(inputData, inputType)` - Analyze mood input
- `addToHistory(moodEntry)` - Add entry to history
- `storeMood(moodData)` - Persist mood to backend
- `clearMood()` - Reset mood state

### Tracker Store (`src/store/trackerStore.js`)
Manages history and journal data:
- `fetchHistory(days)` - Get mood history
- `fetchJournalEntries()` - Get journal entries
- `addJournalEntry(text)` - Create new journal entry
- `getMoodSummary()` - Get 7-day mood analysis

## 🎨 Design Philosophy

- **Calming Aesthetics**: Teal, green, and emerald tones create a peaceful environment
- **Accessibility**: High contrast ratios, readable typography, responsive design
- **Smooth Interactions**: Framer Motion animations provide fluid transitions
- **Minimalist UI**: Clean cards, rounded corners, intentional whitespace
- **Mobile-First**: Responsive layout works seamlessly on all devices

## 📱 Responsive Design

The application is fully responsive and optimized for:
- Mobile devices (320px and up)
- Tablets (768px and up)
- Desktop (1024px and up)

## 🔐 Security Considerations

- API calls are abstracted in the `api.js` service layer
- Sensitive data should be handled securely on the backend
- JWT tokens for authentication should be implemented in production
- Environment variables should never include sensitive credentials

## 🚧 Mock Data

The application includes mock data fallback for development:
- Mock mood analysis with personalized messages
- Mock 7-day history
- Mock journal entries

When backend is unavailable, the app gracefully displays mock data with an info message.

## 📦 Build Output

Production build generates optimized assets in the `dist/` folder:
- Minified CSS (~3.57 KB gzipped)
- Minified JavaScript (~205 KB gzipped)
- Optimized images and assets

## 🔮 Backend Integration

To integrate with a Node.js + Express + Mongoose backend:

1. Update `VITE_API_URL` in your `.env` file
2. Implement the API endpoints specified in the [API Endpoints](#-api-endpoints-ready-for-backend-integration) section
3. Ensure your backend returns data in the expected format:
   ```json
   {
     "mood": "peaceful",
     "message": "Your mind reflects the stillness of a serene lake...",
     "suggestions": ["Meditation", "Nature walk"],
     "timestamp": "2024-01-15T10:30:00Z"
   }
   ```

## 🛠️ Development Commands

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build
- `npm run typecheck` - Check TypeScript types

## 📝 Project Structure Notes

- Each component is self-contained with clear responsibilities
- Zustand stores handle all business logic separate from UI
- API calls are centralized in the service layer
- Tailwind CSS provides consistent styling
- Comments indicate where backend/AI logic will be integrated

## 🌍 Inspiration

This project draws inspiration from:
- Meditation and wellness apps (Calm, Headspace)
- Emotion tracking tools
- Mindfulness practices
- Sanskrit philosophy and wellness principles

## 📄 License

This project is open source and available for personal and commercial use.

## 🤝 Support

For questions or issues, please refer to the inline comments in the codebase, particularly in:
- `src/store/moodStore.js` - Mood analysis logic
- `src/store/trackerStore.js` - History and journal management
- `src/api/api.js` - Backend connection points

---

**Made with heart for emotional wellness and self-discovery**
