# AI-Human Symbiosis Dashboard

## Project Overview
An interactive web dashboard exploring the symbiotic relationship between AI and humans in critical domains: Life Sciences and Human Spaceflight. The project demonstrates the principle of "Vivre Ensemble" (Living Together) - showing how AI should serve as a collaborative tool rather than an autonomous decision-maker.

## Purpose
To educate and demonstrate:
- The difference between AI-assisted and AI-autonomous decision-making
- Why human authority must be retained in critical domains
- The importance of cooperation over control in AI alignment
- Real-world scenarios where AI-human collaboration saves lives

## Technology Stack
- **Frontend**: React 19 with TypeScript
- **Backend**: Express.js (Node.js)
- **Build Tool**: Vite 7
- **AI Services**: OpenAI (GPT-5, text-embedding-3-small)
- **Vector Database**: Vectra (local file-based)
- **PDF Processing**: pdf-parse v2.x
- **Styling**: Custom CSS with responsive design
- **Deployment**: Frontend on port 5000, Backend API on port 3000

## Project Structure
```
/
├── src/
│   ├── App.tsx              # Main dashboard component with scenarios
│   ├── App.css              # Dashboard styling
│   ├── AITraining.tsx       # RAG training interface component
│   ├── AITraining.css       # RAG interface styling
│   ├── main.tsx             # React entry point
│   └── index.css            # Global styles
├── server/
│   ├── index.ts             # Express API server for RAG operations
│   └── tsconfig.json        # Server TypeScript configuration
├── uploads/                 # Temporary file upload directory
├── vector-index/            # Vectra vector database storage
├── index.html               # HTML template
├── vite.config.ts           # Vite configuration (host: 0.0.0.0, port: 5000)
├── tsconfig.json            # TypeScript configuration
└── package.json             # Dependencies and scripts
```

## Key Features

### 1. Interactive Scenarios
Six real-world scenarios across two domains:
- **Life Sciences**: Cancer treatment, drug interactions, epidemic response
- **Human Spaceflight**: Life support failures, debris collision, crew psychology

### 2. Decision-Making Comparison
Each scenario shows:
- **AI-Assisted**: AI provides analysis, humans make final decision (recommended)
- **AI-Autonomous**: AI makes decision automatically (shows risks)

### 3. Educational Insights
- Core principles of AI-human symbiosis
- Why certain approaches work or fail
- Accountability and trust considerations

### 4. AI Training with RAG (New!)
Interactive demonstration of Retrieval-Augmented Generation:
- **Upload Lecture Notes**: Upload PDF or TXT files containing educational content
- **Ask Questions**: Query the AI using your uploaded lecture materials
- **Source Attribution**: See exactly which parts of your lectures the AI used
- **RAG vs Fine-Tuning**: Educational comparison of the two approaches
- Demonstrates the "Option 3" approach - using RAG for training AI with custom data

## Core Philosophy

### Vivre Ensemble (Living Together)
AI and humans coexist in a partnership where:
- AI provides rapid analysis, pattern recognition, scenario simulation
- Humans provide contextual judgment, ethical reasoning, empathy, accountability
- Together they make faster, more informed decisions that respect human values

### The Prisoner's Dilemma Insight
If we design AI alignment as pure control, we create adversarial relationships. Instead, we design for cooperation where both AI and humans benefit from collaboration.

### No Harm Foundation
AI systems must understand context, culture, and long-term consequences. "Do no harm" includes recognizing when inaction itself causes harm.

## Running the Project
```bash
npm install
npm run dev:all  # Runs both frontend and backend concurrently
```
- **Frontend Dashboard**: http://localhost:5000
- **Backend API**: http://localhost:3000/api

Or run separately:
```bash
npm run dev      # Frontend only
npm run server   # Backend only
```

## Recent Changes
- **2025-10-31**: Added AI Training capabilities with RAG
  - Built Express.js backend API server for RAG operations
  - Integrated Vectra local vector database for embeddings
  - Implemented OpenAI GPT-5 and text-embedding-3-small
  - Created interactive upload interface for lecture notes (PDF/TXT)
  - Built Q&A interface with source attribution
  - Added educational RAG vs Fine-Tuning comparison
  - Demonstrates practical RAG implementation (Option 3)
  - Configured concurrent workflow for frontend + backend

- **2025-10-24**: Initial project creation
  - Set up React + Vite + TypeScript
  - Created interactive dashboard with 6 scenarios
  - Implemented domain filtering (All/Life Sciences/Spaceflight)
  - Added comparison views for AI-assisted vs AI-autonomous
  - Styled with gradient backgrounds and responsive design
  - Configured Vite for Replit environment (allowedHosts: true)

## User Preferences
- Focus on Life Sciences and Human Spaceflight applications
- Emphasize AI as a tool, not autonomous decision-maker
- Long-term mission: demonstrate symbiotic AI-human coexistence
- Interactive, educational approach to complex topics

## Important Notes

### OpenAI API Setup
The AI Training feature requires an OpenAI API key with available credits:
1. Make sure your API key is set in Replit Secrets (OPENAI_API_KEY)
2. Ensure your OpenAI account has sufficient credits
3. The system uses:
   - GPT-5 for generating answers
   - text-embedding-3-small for creating embeddings

### RAG Feature Usage
1. Upload lecture notes (PDF or TXT format) via the Upload tab
2. The system will chunk the text and create embeddings
3. Ask questions in the Ask Questions tab
4. The AI will retrieve relevant content and cite sources
5. View the RAG vs Fine-Tuning comparison to understand the approach
