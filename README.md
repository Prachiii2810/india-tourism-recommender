# 🗺️ Smart India Tourism Explorer & AI Recommender System

An AI-powered web application designed to help travelers discover optimal tourist destinations across India. This project utilizes a content-based filtering mechanism powered by Cosine Similarity to recommend mathematically similar attractions based on location, regional significance, travel category, and optimal visiting windows.

Built as a capstone submission for the **IBM 6-Week AI Virtual Internship Framework**.

Live Production App Link: https://india-tourism-recommender.streamlit.app/

---

## 🚀 Key Features

- **🤖 Machine Learning Recommendation Engine:** Uses natural language processing (NLP) tokenization and vector similarity scoring to suggest the top 5 closest matches to any selected base attraction.
- **🧭 Dynamic Trip Planner Sandbox:** Interactive sidebar controls allow users to slice and dice the tourism dataset based on maximum entrance fees (budget constraints), maximum travel durations, state filters, and utility perks (e.g., DSLR photography rules or proximity to an airport).
- **📊 Real-time Analytical Metrics:** Dynamic dashboard components recalculate and display running statistical highlights—such as sample destination densities and average user ratings—instantly.

---

## 🛠️ The Architecture & ML Strategy

The backend processes raw domain metadata to calculate a mathematical similarity score across locations.

1. **Feature Engineering (Metadata Soup):** String values for categorical parameters (`Type`, `Significance`, `Zone`, `State`, and `Best Time to visit`) are sanitized and concatenated into a centralized feature block.
2. **Text Vectorization:** A Scikit-Learn `CountVectorizer` passes through the data matrix, stripping English stop words and generating numerical token counts.
3. **Cosine Similarity Evaluation:** The app calculates the angular cosine distance between multi-dimensional vectors to determine contextual similarity:

$$\text{Similarity} = \cos(\theta) = \frac{\mathbf{A} \cdot \mathbf{B}}{\|\mathbf{A}\| \|\mathbf{B}\|}$$

---

## 📂 Repository Structure

The project workspace follows this structured framework:
```text
├── app.py                  # Streamlit Web User Interface & Engine Execution Logic
├── indian tourism.csv      # Cleaned India Tourism Source Dataset
├── requirements.txt        # Production Cloud Dependency Installer Manifest
└── README.md               # Professional Internship Project Documentation
