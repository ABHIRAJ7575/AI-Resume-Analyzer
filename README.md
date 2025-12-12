# AI Resume Analyzer

A premium web application that provides intelligent resume analysis and interview preparation tools powered by Google Gemini AI. Features a stunning dark theme interface with professional-grade animations and visual effects.

## 📚 Documentation

- **[Quick Start Guide](./QUICK_START.md)** - Get started in 5 minutes ⚡
- **[Architecture Overview](./ARCHITECTURE.md)** - System design and data flow 🏗️
- **[Project Structure](./PROJECT_STRUCTURE.md)** - Detailed file organization 📁
- **[Backend Documentation](./backend/README.md)** - Backend API details 🔧

## Features

- 🎨 **Premium UI/UX**: Dark/Light theme with metallic gradients, glassmorphism effects, and smooth micro-interactions
- 📄 **PDF Upload**: Drag-and-drop interface with advanced PDF viewer (zoom, navigation, keyboard shortcuts)
- 🤖 **AI Analysis**: Intelligent resume analysis with detailed scoring and improvement suggestions powered by Google Gemini
- 💼 **Interview Prep**: AI-generated interview questions with categorization and difficulty levels
- 📊 **Visual Analytics**: Animated score gauges, breakdown metrics, and statistics dashboard
- 💾 **Export Options**: Export analysis and questions as PDF, text file, or copy to clipboard
- 📱 **Responsive Design**: Collapsible panels for mobile, optimized layouts for tablet and desktop
- ⚡ **Fast Performance**: Lazy loading, debounced API calls, and optimized rendering
- ♿ **Accessible**: WCAG compliant with keyboard navigation and screen reader support
- 🎭 **Theme Switching**: Seamless dark/light mode with localStorage persistence

## Tech Stack

### Frontend
- **Framework**: React 18 + TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Animations**: Framer Motion
- **PDF Processing**: PDF.js
- **UI Components**: lucide-react, react-dropzone, react-hot-toast

### Backend
- **Framework**: Python Flask
- **AI Service**: Google Gemini API
- **PDF Processing**: PyPDF2
- **CORS**: Flask-CORS

## Prerequisites

Before you begin, ensure you have the following installed on your laptop:

- **Node.js 18+** - [Download here](https://nodejs.org/)
- **Python 3.9+** - [Download here](https://www.python.org/downloads/)
- **npm, yarn, or pnpm** - Comes with Node.js (npm) or install separately
- **Git** - [Download here](https://git-scm.com/downloads)
- **Google Gemini API Key** - [Get one free here](https://makersuite.google.com/app/apikey)

### Verify Prerequisites

Open your terminal/command prompt and verify installations:

```bash
node --version    # Should show v18.0.0 or higher
npm --version     # Should show 9.0.0 or higher
python --version  # Should show 3.9.0 or higher
git --version     # Should show 2.0.0 or higher
```

## 🚀 First-Time Setup Guide

Follow these steps to run the project on your laptop for the first time:

### Step 1: Clone the Repository

Open your terminal/command prompt and run:

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-resume-analyzer.git

# Navigate into the project directory
cd ai-resume-analyzer
```

### Step 2: Install Frontend Dependencies

```bash
# Install all frontend dependencies
npm install

# OR if you prefer yarn
yarn install

# OR if you prefer pnpm
pnpm install
```

This will install all required packages listed in `package.json`. It may take 2-3 minutes.

### Step 3: Set Up Backend

#### 3.1 Navigate to Backend Directory

```bash
cd backend
```

#### 3.2 Create Python Virtual Environment

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

You should see `(venv)` in your terminal prompt, indicating the virtual environment is active.

#### 3.3 Install Python Dependencies

```bash
pip install -r requirements.txt
```

This installs Flask, PyPDF2, Google Gemini SDK, and other required packages.

### Step 4: Configure Environment Variables

#### 4.1 Frontend Configuration

Navigate back to the root directory:

```bash
cd ..
```

Create a `.env` file in the root directory:

```bash
# On Windows
copy .env.example .env

# On macOS/Linux
cp .env.example .env
```

Edit the `.env` file and add:

```env
VITE_API_URL=http://localhost:5000
```

#### 4.2 Backend Configuration

Navigate to the backend directory:

```bash
cd backend
```

Create a `.env` file in the backend directory:

```bash
# On Windows
copy .env.example .env

# On macOS/Linux
cp .env.example .env
```

Edit the `backend/.env` file and add your Google Gemini API key:

```env
GEMINI_API_KEY=your_actual_api_key_here
FLASK_ENV=development
CORS_ORIGINS=http://localhost:5173
PORT=5000
```

**⚠️ Important:** Replace `your_actual_api_key_here` with your actual Google Gemini API key from [Google AI Studio](https://makersuite.google.com/app/apikey).

### Step 5: Start the Application

You need to run both the backend and frontend servers.

#### 5.1 Start Backend Server (Terminal 1)

In the `backend` directory with virtual environment activated:

```bash
# Make sure you're in the backend directory
cd backend

# Activate virtual environment if not already active
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate

# Start the Flask server
python app.py
```

You should see:
```
 * Running on http://localhost:5000
 * Debug mode: on
```

**Keep this terminal running!**

#### 5.2 Start Frontend Server (Terminal 2)

Open a **new terminal** window, navigate to the project root, and run:

```bash
# Navigate to project root
cd ai-resume-analyzer

# Start the frontend development server
npm run dev

# OR
yarn dev

# OR
pnpm dev
```

You should see:
```
  VITE v5.0.0  ready in 500 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
```

### Step 6: Open the Application

Open your web browser and navigate to:

```
http://localhost:5173
```

🎉 **Congratulations!** The AI Resume Analyzer is now running on your laptop!

## 📖 How to Use

1. **Upload Resume**: Drag and drop a PDF resume or click to browse
2. **View Analysis**: See detailed ATS score, strengths, and suggestions
3. **Generate Questions**: Click to generate interview questions based on the resume
4. **Export Results**: Export analysis or questions as PDF, text, or copy to clipboard
5. **Switch Theme**: Toggle between dark and light mode using the theme button

## 🛑 Stopping the Application

To stop the servers:

1. **Frontend**: Press `Ctrl + C` in the frontend terminal
2. **Backend**: Press `Ctrl + C` in the backend terminal
3. **Deactivate Python venv**: Type `deactivate` in the backend terminal

## 🔄 Running Again Later

After the first-time setup, you only need to:

1. **Start Backend**:
   ```bash
   cd backend
   venv\Scripts\activate  # Windows
   # OR
   source venv/bin/activate  # macOS/Linux
   python app.py
   ```

2. **Start Frontend** (new terminal):
   ```bash
   npm run dev
yarn install
# or
pnpm install
```

### 3. Configure Environment Variables

#### Frontend Configuration

Create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Edit the `.env` file:

```env
VITE_API_URL=http://localhost:5000
```

#### Backend Configuration

Create a `.env` file in the `backend` directory:

```bash
cd backend
cp .env.example .env
```

Edit the `backend/.env` file and add your Google Gemini API key:

```env
GEMINI_API_KEY=your_actual_api_key_here
FLASK_ENV=development
CORS_ORIGINS=http://localhost:5173
PORT=5000
```

**Important**: Never commit your `.env` files to version control. They're already included in `.gitignore`.

### 4. Start the Backend Server

```bash
cd backend
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

pip install -r requirements.txt
python app.py
```

The backend will run on [http://localhost:5000](http://localhost:5000).

### 5. Start the Frontend Development Server

In a new terminal:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

## Building for Production

```bash
npm run build
# or
yarn build
# or
pnpm build
```

The optimized production build will be in the `dist` directory.

### Preview production build

```bash
npm run preview
# or
yarn preview
# or
pnpm preview
```

## Project Structure

```
ai-resume-analyzer/
├── 📁 src/                          # Frontend source code
│   ├── 📁 components/               # React components
│   │   ├── 📁 ui/                  # Reusable UI components
│   │   │   ├── AnimatedSection.tsx # Animated wrapper component
│   │   │   ├── Button.tsx          # Custom button with animations
│   │   │   ├── FunLoadingMessages.tsx # Rotating loading messages
│   │   │   ├── GlassCard.tsx       # Glassmorphism card
│   │   │   ├── LoadingSkeleton.tsx # Loading placeholder
│   │   │   ├── LoadingSpinner.tsx  # Animated spinner
│   │   │   └── index.ts            # UI exports
│   │   ├── AnalysisResults.tsx     # Resume analysis display
│   │   ├── AnimatedBackground.tsx  # Animated background
│   │   ├── ErrorBoundary.tsx       # Error handling wrapper
│   │   ├── Footer.tsx              # App footer
│   │   ├── Header.tsx              # App header
│   │   ├── InterviewQuestions.tsx  # Questions display
│   │   ├── OfflineIndicator.tsx    # Network status indicator
│   │   ├── PDFPreview.tsx          # PDF viewer component
│   │   ├── QuestionCard.tsx        # Individual question card
│   │   ├── SplitLayout.tsx         # Two-column layout
│   │   ├── UploadContainer.tsx     # Upload wrapper
│   │   └── UploadZone.tsx          # Drag-drop upload area
│   ├── 📁 hooks/                   # Custom React hooks
│   │   ├── useAnalysis.ts          # Resume analysis logic
│   │   ├── useAnimationFallback.ts # Animation fallback
│   │   ├── useFileUpload.ts        # File upload handling
│   │   ├── useNetworkStatus.ts     # Network monitoring
│   │   └── useReducedMotion.ts     # Accessibility motion
│   ├── 📁 services/                # API & services
│   │   ├── apiClient.ts            # Backend API client
│   │   └── index.ts                # Service exports
│   ├── 📁 styles/                  # Global styles
│   │   └── globals.css             # Tailwind + custom CSS
│   ├── 📁 test/                    # Test configuration
│   │   └── setup.ts                # Vitest setup
│   ├── 📁 types/                   # TypeScript definitions
│   │   └── index.ts                # Type exports
│   ├── 📁 utils/                   # Utility functions
│   │   ├── animations.ts           # Animation configs
│   │   ├── confetti.ts             # Confetti effects
│   │   ├── downloadResults.ts      # Download functionality
│   │   ├── performance.ts          # Performance utilities
│   │   └── index.ts                # Utility exports
│   ├── App.tsx                     # Main app component
│   ├── main.tsx                    # React entry point
│   └── vite-env.d.ts              # Vite type definitions
│
├── 📁 backend/                     # Python Flask backend
│   ├── 📁 services/                # Backend services
│   │   ├── ai_service.py           # Google Gemini AI integration
│   │   └── pdf_service.py          # PDF text extraction
│   ├── 📁 tests/                   # Backend tests
│   │   ├── conftest.py             # Pytest configuration
│   │   ├── test_ai_service.py      # AI service tests
│   │   ├── test_api_endpoints.py   # API endpoint tests
│   │   └── test_pdf_service.py     # PDF service tests
│   ├── app.py                      # Flask application
│   ├── requirements.txt            # Python dependencies
│   ├── pytest.ini                  # Pytest config
│   ├── .env.example                # Environment template
│   └── README.md                   # Backend documentation
│
├── 📁 public/                      # Static assets
│   └── (favicon, images, etc.)
│
├── 📁 .kiro/                       # Kiro IDE configuration
│   └── specs/                      # Project specifications
│
├── 📄 Configuration Files
│   ├── .env                        # Frontend environment (gitignored)
│   ├── .eslintrc.cjs              # ESLint configuration
│   ├── .gitignore                 # Git ignore rules
│   ├── index.html                 # HTML entry point
│   ├── package.json               # Frontend dependencies
│   ├── postcss.config.js          # PostCSS configuration
│   ├── tailwind.config.js         # Tailwind CSS config
│   ├── tsconfig.json              # TypeScript config
│   ├── tsconfig.node.json         # Node TypeScript config
│   ├── vite.config.ts             # Vite configuration
│   └── README.md                  # This file
│
└── 📄 Test Files
    ├── src/components/AnalysisResults.test.tsx
    ├── src/components/InterviewQuestions.test.tsx
    └── src/services/apiClient.test.ts
```

For detailed information about each directory and file, see [PROJECT_STRUCTURE.md](./PROJECT_STRUCTURE.md).

## Configuration

### Tailwind CSS

The project uses a custom Tailwind theme with:
- Dark color palette (purple, blue, neon accents)
- Custom fonts (Caveat, Permanent Marker, Inter)
- Custom animations (gradient, float, glow)
- Glassmorphism utilities

### Vite

Optimized configuration includes:
- Code splitting for vendor chunks
- Minification with Terser
- Optimized dependency pre-bundling

## Environment Variables

### Frontend (.env)

| Variable | Description | Required | Default |
|----------|-------------|----------|---------|
| `VITE_API_URL` | Backend API URL | No | `http://localhost:5000` |

### Backend (backend/.env)

| Variable | Description | Required | Default |
|----------|-------------|----------|---------|
| `GEMINI_API_KEY` | Google Gemini API key for AI analysis | Yes | - |
| `FLASK_ENV` | Flask environment (development/production) | No | `development` |
| `CORS_ORIGINS` | Allowed CORS origins (comma-separated) | No | `http://localhost:5173` |
| `PORT` | Backend server port | No | `5000` |

## Troubleshooting

### Backend Connection Issues

If the frontend can't connect to the backend:
1. Ensure the backend server is running on port 5000
2. Check that `VITE_API_URL` in frontend `.env` matches the backend URL
3. Verify CORS is configured correctly in `backend/.env`

### API Key Issues

If you see an error about missing API key:
1. Ensure `backend/.env` file exists
2. Verify the API key is correctly set: `GEMINI_API_KEY=your_key`
3. Restart the backend server after adding the key

### PDF Upload Issues

- Ensure the file is a valid PDF
- Check file size (recommended < 10MB)
- Try a different PDF if extraction fails

### Build Errors

If you encounter build errors:
```bash
# Clear node_modules and reinstall
rm -rf node_modules package-lock.json
npm install

# Clear Vite cache
rm -rf node_modules/.vite
```

## Performance

- Lighthouse score target: 90+
- First Contentful Paint: < 1.5s
- Time to Interactive: < 3.5s
- Animations run at 60fps

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari 14+, Chrome Android 90+)

## License

MIT

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues and questions, please open an issue on GitHub.
