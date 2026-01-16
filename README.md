# microbiome_gut_health_assistant
Chatbot with microbiome insights
🧬 MIOME — Gut Health Assistant
here dataset is avalialbe
code file is not provided because of api key present in it

MIOME is an interactive Streamlit web app that helps users analyze their gut health scores and provides personalized advice through a chatbot interface.


🔑 Key Features
📂 Data Upload & Processing

Upload CSV/XLSX files with gut health metrics:

fiber_score, probiotic_score, diversity_score (0–10 scale).

Cleans, validates, and clips scores into a safe range (0–10).




📊 Gut Health Report

Computes an overall Gut Score:

Gut Score = 0.4 × fiber + 0.3 × probiotic + 0.3 × diversity



Categorizes into zones:

🟢 Excellent

🟡 Needs Attention

🔴 Urgent Care


Displays individual metrics on a dashboard.

Provides rule-based personalized tips for fiber, probiotics, and dietary diversity.


🤖 Chatbot (MIOME Bot)

NLP-powered intent detection:

✅ SentenceTransformers (all-MiniLM-L6-v2) if available

⚡ TF-IDF + cosine similarity fallback

Recognizes intents:

Greetings, Summary, Detailed Summary, Diet, Improvements

Fiber, Probiotic, Diversity info

Help, Thanks, Goodbye

Supports follow-up conversations (e.g., "yes" → summary).

Optional Google Gemini integration for detailed AI-generated summaries.


🧰 Tech Stack

Frontend/UI: Streamlit

Data Processing: pandas, numpy

ML/NLP: sentence-transformers, scikit-learn (TF-IDF)

AI Integration (Optional): Google Gemini (google-generativeai)


🧠 Example Workflow

Upload a gut health file:

date,fiber_score,probiotic_score,diversity_score
2025-08-01,6,5,7
2025-08-10,7,6,8


App shows:

🌾 Fiber: 7.0/10

🦠 Probiotic: 6.0/10

🥗 Diversity: 8.0/10

➡️ Gut Score: 7.1/10 🟡 Needs Attention

💡 Personalized Tip:

🌾 Fiber: add legumes, whole grains, veggies, and fruit skins

🦠 Probiotics: include yogurt/kefir or fermented foods daily

🥗 Diversity: rotate 20–30 plant foods weekly



Chat with MIOME:
User: Show me my summary
Bot:

📊 Report Summary:
- 🌾 Fiber: 7.0/10
- 🦠 Probiotic: 6.0/10
- 🥗 Diversity: 8.0/10
➡️ Gut Score: 7.1/10 (Needs Attention)

💡 Tip: Add fiber, probiotics, and plant diversity as above.




Install dependencies:

pip install -r requirements.txt



(Optional) Set your Gemini API Key in app.py:

GEMINI_API_KEY = "your_api_key_here"


Run the app:

streamlit run app.py



🙌 Acknowledgments

Streamlit
 — UI framework

SentenceTransformers
 — NLP embeddings

scikit-learn
 — fallback intent detection

Developer: Manish M Kumar
