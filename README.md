# SkillMatch AI

SkillMatch AI is an advanced AI-powered workforce intelligence platform designed to analyze skills from resumes and job descriptions, provide personalized career recommendations, forecast market trends, and generate personalized learning paths. It utilizes large language models, knowledge graphs, and embeddings to deliver actionable insights for employees and organizations.

---

## Features

- AI-driven skill extraction from resumes, job descriptions, and manual inputs
- Skill comparison for multiple candidates against job descriptions
- Personalized career path recommendations with growth potential and learning resources
- Market trending skills and demand forecasting with dynamic visualizations
- Neo4j knowledge graph integration for skill relationships and recommendations
- Interactive and user-friendly Streamlit frontend

---

## Project Structure

```
SkillMatchAI/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── __init__.py
│   │   │   ├── dependencies.py
│   │   │   ├── routes.py
│   │   ├── database/
│   │   │   ├── __init__.py
│   │   │   ├── connection.py
│   │   │   └── models.py
│   │   ├── services/
│   │   │   ├── __init__.py
│   │   │   ├── forecasting_agent.py
│   │   │   ├── recommendation_agent.py
│   │   │   ├── skill_extraction_agent.py
│   │   │   └── skill_graph_service.py
│   │   ├── utils/
│   │   │   ├── __init__.py
│   │   │   └── helpers.py
│   │   ├── config.py
│   │   ├── main.py
│   │   └── run.py
│   ├── requirements.txt
│   └── .env
├── frontend/
│   ├── components/
│   │   ├── __init__.py
│   │   ├── api_client.py
│   │   └── skill_visualizer.py
│   ├── pages/
│   │   ├── Career_Recommendations.py
│   │   ├── Dashboard.py
│   │   ├── Learning_Path.py
│   │   ├── Market_Insights.py
│   │   ├── Resume_Comparison.py
│   │   └── Skill_Analysis.py
│   ├── utils/
│   │   ├── __init__.py
│   │   └── helpers.py
│   ├── config.py
│   ├── requirements.txt
│   └── streamlit_app.py
├── README.md
```

---

## Prerequisites

- Python 3.10+
- Neo4j Database configured with credentials in `.env`
- Ollama LLM running locally with the Llama 3.2 model downloaded
- Virtual environment for backend and frontend dependencies

---

## Installation & Setup

### Backend

1. Navigate to backend directory, create and activate virtual environment:

```
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

2. Install backend dependencies:

```
pip install -r requirements.txt
```

3. Download spaCy model:

```
python -m spacy download en_core_web_sm
```

4. Setup `.env` file with necessary environment variables:

```
NEO4J_URI=neo4j://127.0.0.1:7687
NEO4J_USER=neo4j
NEO4J_PASSWORD=Harsh@123
NEO4J_DATABASE=skillmatch

OLLAMA_BASE_URL=http://localhost:11434
OLLAMA_MODEL=llama3.2

SECRET_KEY=your_secret_key_here
DATABASE_URL=sqlite:///./skillmatch.db
ENVIRONMENT=development
DEBUG=True
```

5. Run backend server:

```
python run.py
```

---

### Frontend

1. Navigate to frontend directory and setup virtual environment:

```
cd frontend
python -m venv venv
source venv/bin/activate
```

2. Install frontend dependencies:

```
pip install -r requirements.txt
```

3. Run Streamlit app:

```
streamlit run streamlit_app.py
```

Open your browser to `http://localhost:8501`

---

## Usage

- Use **Skill Analysis** page to analyze resumes or job descriptions.
- Use **Resume Comparison** page to compare multiple CVs against a job description.
- View **Career Recommendations** personalized to your skill profile.
- Explore **Market Insights** for trending skills and forecasts.
- Generate **Learning Paths** personalized per skill and expertise level.

---

## Troubleshooting

- Ensure Ollama service is running at `http://localhost:11434`
- Ensure Neo4j database is running with correct credentials
- Run Streamlit and backend from correct directories
- Remove emojis or special characters from page file names
- Clear Streamlit cache when switching pages: `streamlit cache clear`

---

## License

This project is licensed under the MIT License.

---

## Contact

For support or questions, contact me.

---

*Powered by Generative AI.*
