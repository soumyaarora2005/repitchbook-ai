💡RepitchBook

AI-Powered Real Estate Deal Intelligence Engine, to refine, structure, and repitch ideas effectively

Transform raw property data into institutional-grade investment memos in seconds — powered by Groq's ultra-fast LLaMA 3.3 70B model.

<img width="1911" height="1002" alt="image" src="https://github.com/user-attachments/assets/6dd8832a-37a0-4452-a606-4f1bbc09f64c" />


📌 Abstract

REPitchBook AI is a full-stack AI-powered real estate investment analysis platform. It takes property details such as purchase price, expected rent, annual costs, and location to instantly generate a structured and professional-grade investment memo completed with ROI, rental yield, cash flow analysis, market context and a final recommendation.
Built for real estate investors, analysts and fund managers who need fast and reliable deal screening without manual number-crunching or generic chatbot responses.

✨ Features

- AI Memo Generation — Generates institutional-quality investment memos using Groq's LLaMA 3.3 70B model
- Automated Financial Metrics — Calculates ROI, rental yield, annual cash flow, and investment score automatically
- Market Context Analysis — Pulls real-time market data to contextualize each deal
- Structured Output — Every memo includes Investment Thesis, Key Strengths, Risk Factors, Market Positioning, and Final Recommendation
-  Ultra-Fast Inference — Powered by Groq for near-instant AI responses
- Secure API Handling — Environment-based key management, no keys exposed to client
- REST API — Clean FastAPI backend with full Swagger documentation at /docs
- Responsive Frontend — React + Vite frontend with Tailwind CSS, works on all devices


🛠️ Tech Stack
- Backend
    Technology:                                             Purpose:
    - Python 3.14                                           Core language
    - FastAPI                                               REST API framework
    - Uvicorn                                               ASGI server
    - Groq SDK                                              AI inference (LLaMA 3.3 70B)
    - Pydantic                                              Data validation and modeling
    - python-dotenv                                         Environment variable management
    - httpx                                                 Async HTTP client
      
- Frontend
  Technology:                                               Purpose:
    - React                                                 UI framework
    - Vite                                                  Build tool and dev server
    - TypeScript                                            Type-safe JavaScript
    - Tailwind CSS                                          Utility-first styling
    - Node.js                                               Runtime environment
      
- Infrastructure
   Service:                                                 Purpose:
    - Render                                                Backend deployment
    - Vercel                                                Frontend deployment
    - GitHub                                                Version control
    - Groq Cloud                                            AI model hosting


📸 Screenshots

Dashboard / Home

<img width="1919" height="996" alt="image" src="https://github.com/user-attachments/assets/2914fbf9-7226-4cf1-8682-e95f7ae9d887" />

Deal Analysis Form

<img width="1919" height="999" alt="image" src="https://github.com/user-attachments/assets/6964e213-2da9-41c5-abe0-668083afa40d" />

Generated Investment Memo and Reports

<img width="1919" height="991" alt="image" src="https://github.com/user-attachments/assets/77bbf362-ccd8-4215-a539-6547f792c949" />


<img width="1919" height="1008" alt="image" src="https://github.com/user-attachments/assets/e746db46-8937-477f-950c-793c6c31a8a1" />


⚙️ Installation & Local Setup
Prerequisites-

Make sure you have these installed:

- Python 3.10+
- Node.js 18+
- Git
- A Groq API Key (free)


1. Clone the Repository:
2. 
    bash
   
    git clone https://github.com/soumyaarora2005/repitchbook-ai.git
   
    cd repitchbook-ai

4. Backend Setup:
   
    bash
   
    # Install Python dependencies
   
    pip install -r requirements.txt
   

    - Create a .env file in the root directory:
      
       env
      
       GROQ_API_KEY=your_groq_api
      
    - Start the backend server:
       bash
      
       # Windows
      
       python -m uvicorn app.main:app --reload

       # Mac/Linux
      
       uvicorn app.main:app --reload
      
Backend runs at → http://localhost:8000

API Docs at → http://localhost:8000/docs

3. Frontend Setup:
   
    bash
   
    cd frontend

   # Install dependencies
   
   npm install
   
   - Create a .env file inside the frontend folder:
     
      env
     
      VITE_API_BASE_URL=http://localhost:8000
     
   - Start the frontend:
     
      bash
     
      npm run dev
     
Frontend runs at → http://localhost:8080

4. Running Both Servers:
   
Open two terminals and run simultaneously:

Terminal                Command                                                              URL

Terminal 1              (Backend)python -m uvicorn app.main:app --reload                     http://localhost:8000

Terminal 2              (Frontend)cd frontend && npm run dev                                 http://localhost:8080


🚀 Deployment
Backend → Render

Push your code to GitHub
Go to render.com → New Web Service
Connect your GitHub repo
Use these settings:

Field                    Value                     
Root Directory           (leave empty)
Runtime                  Python 3
Build Command            pip install -r requirements.txt
Start Command            uvicorn app.main:app --host 0.0.0.0 --port 8000

Add environment variable:

GROQ_API_KEY =your_groq_api
Click Create Web Service


Frontend → Vercel

Go to vercel.com → Add New Project
Import your GitHub repo
Use these settings:

Field                   Value
Root Directory          frontend
Framework Preset        Vite
Build Command           npm run build
Output Directory        dist

Add environment variable:

VITE_API_BASE_URL = https://repitchbook-ai.onrender.com

Click Deploy



📄 Live Demo 
https://repitchbook-ai-a3s1.vercel.app



👥 Contributors

| Soumya Arora | [@soumyaarora2005](https://github.com/soumyaarora2005) |

| Siddharth Doda | [@Siddharth-Doda](https://github.com/Siddharth-Doda) |




👤 Author
Soumya Arora


GitHub: soumyaarora2005

LinkedIn: https://www.linkedin.com/in/soumya-arora-62t007770n




