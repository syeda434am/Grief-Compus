# Grief Compass 🎗️

<a href="https://grief-compus.onrender.com/">
  <img src="com/mhire/ui/public/live-demo.png" alt="Live Demo" width="100" />
</a>

Grief Compass is a comprehensive digital platform designed to provide personalized support and guidance for individuals navigating through grief. By combining AI with empathetic design, this platform offers tailored resources, daily schedules, and interactive tools to help users process their grief journey in a healthy and supported way.

![Grief Compass](com/mhire/ui/public/gc.png)

## 🌟 Key Features

- 📅 **Daily Schedule Builder** - Structured daily activities to maintain routine and wellness
- 🗣️ **Interactive Grief Guide** - Conversational interface for immediate emotional support
- 📊 **Sentiment Analysis** - Track and understand emotional patterns over time

## 🛠️ Technology Stack

- 🚀 **FastAPI** – High-performance Python-based backend with async capabilities
- 🧠 **AI Integration** – Backend powered by advanced AI model (Meta Llama 3 70b)
- ⚡️ **Vite** - Lightning fast build tool
- 🔥 **React 18** - Latest React features
- 🧩 **TypeScript** - Type safety for better developer experience
- 🎨 **TailwindCSS** - Utility-first CSS framework
- 🧰 **ShadCN UI** - Accessible and customizable UI components
- 📱 **Responsive Design** - Mobile-first approach
- 🧭 **React Router** - Easy client-side routing
- 🔄 **React Query** - Data fetching and state management
- 🧪 **Form Handling** - React Hook Form with Zod validation

## 🚀 Getting Started

### Prerequisites

#### Frontend Requirements
- Node.js 18+ 
- npm, yarn, or pnpm

#### Backend Requirements
- Python 3.10+
- pip
- FastAPI

### Installation

1. Clone this repository:
```bash
git clone https://github.com/your-username/Grief-Compass.git
cd Grief-Compass
```

2. Install frontend dependencies:
```bash
npm install
# or
yarn
# or
pnpm install
```

3. Install backend dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file in the root directory with:
```env
GROQ_API_KEY=your_groq_api_key
GROQ_MODEL_NAME=your_model_name
TAVILY_API_KEY=your_tavily_api_key
VITE_API_BASE_URL=http://localhost:8000
```

5. Make sure to edit the project structure as mentioned in 'Project Structure' section

6. Start the backend server:
```bash
uvicorn com.mhire.app.main:app --reload
```

7. Start the frontend development server:
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

8. Open your browser and visit `http://localhost:8080`

## 📁 Project Structure
- Set the project within below structure by copying the files and folders inside com/mhire/ui/ and paste them outside of the com folder. The structure will then look like below:
```
grief-compass/
├── com/                 # Backend Python package
│   └── mhire/app/
│       ├── main.py     # FastAPI application entry
│       ├── common/     # Shared utilities
│       ├── config/     # Configuration management
│       └── services/   # Backend services
│           ├── personalized_content/
│           ├── schedule_builder/
│           └── sentiment_toolkit/
├── src/                # Frontend source code
│   ├── components/     # React components
│   │   └── ui/        # ShadCN UI components
│   ├── hooks/         # Custom React hooks
│   ├── lib/           # Utility functions
│   ├── pages/         # Page components
│   ├── App.tsx        # Main React component
│   ├── index.css      # Global styles
│   └── main.tsx       # Frontend entry point
├── public/            # Static assets
├── nginx/             # Nginx configuration
├── requirements.txt   # Python dependencies
├── package.json       # Node.js dependencies
└── docker-compose.yml # Docker configuration
```

## 🔧 API Endpoints

### Personalized Content
- `POST /api/personalized-content` - Generate personalized grief support content

### Schedule Builder
- `POST /api/schedule` - Create a personalized daily schedule

### Sentiment Analysis
- `POST /api/sentiment` - Analyze text for emotional content

## 🚀 Deployment

The application is deployed on Render as the Web Service under a particular project (backend and frontend running on two different services)

### Environment Variables Required for Deployment
```env
GROQ_API_KEY=your_groq_api_key
GROQ_MODEL_NAME=your_model_name
TAVILY_API_KEY=your_tavily_api_key
VITE_API_BASE_URL=your_production_api_url
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
