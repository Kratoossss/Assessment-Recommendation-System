# **Assessment Recommendation System**

An AI-powered recommendation system designed to suggest the most relevant SHL assessments based on user queries, job descriptions, or unstructured input data. This system leverages NLP techniques and Large Language Models (LLMs) to deliver accurate, efficient, and context-aware results through an intuitive frontend interface.

---

## **Features**

- **Custom Recommendations**:
  - Based on job descriptions, unstructured text, or user queries.
- **Advanced NLP Techniques**:
  - Semantic similarity matching using Sentence-BERT.
- **LLM Integration**:
  - Contextual feature extraction using Gemini 1.5 Pro.
- **Efficient Ranking**:
  - Cosine similarity for scoring and ranking assessments.
- **Interactive Frontend**:
  - Streamlit-based interface for seamless user interaction.

---

## **Tech Stack**

### **Natural Language Processing (NLP)**:
- **Sentence-BERT**: Converts assessments and queries into embeddings.
- **Cosine Similarity**: Ranks assessments based on semantic relevance.

### **LLM Integration**:
- **Gemini 1.5 Pro**:
  - Extracts structured features (e.g., job roles, skills, duration) from unstructured input.
  - Enhances recommendations with contextual filtering.

### **Frontend**:
- **Streamlit**: Provides an interactive and user-friendly interface.

---

## **How It Works**

1. **Data Preparation**:
   - A dataset of 50 SHL-like assessments is used, containing:
     - Assessment name, URL, duration, test type, skills, description, remote support, and adaptive/IRT support.
   - A "combined" column is created by concatenating all fields for embedding.

2. **NLP Embedding & Retrieval**:
   - Sentence-BERT generates vector embeddings for both dataset entries and user queries.
   - Cosine similarity identifies the top matching assessments.

3. **LLM Enhancement**:
   - Gemini 1.5 Pro processes unstructured input (e.g., job descriptions, URLs).
   - Extracted features (e.g., skills, duration) are used to refine recommendations.

4. **Evaluation**:
   - Recommendations are ranked and filtered based on relevance and constraints (e.g., duration, skills).

5. **Streamlit Interface**:
   - Users input queries via a web interface.
   - The system displays top recommendations with detailed information.

---

## **Performance**

- **NLP Model**:
  - Recall@5: **0.85**
  - MAP@5: **0.71**
- **NLP + LLM Model**:
  - Recall@5: **1.0**
  - MAP@5: **1.0**

---

## **Example Use Cases**

1. **Java Developer Hiring**:
   - "Looking for Java developers who can collaborate effectively with business teams. Assessments should be completed in 40 minutes."
2. **Mid-Level Professionals**:
   - "Need an assessment package for Python, SQL, and JavaScript skills with a maximum duration of 60 minutes."
3. **Analyst Screening**:
   - "Looking for cognitive and personality tests to screen analyst candidates."
4. **Teamwork & Communication**:
   - "Want to assess communication and teamwork skills in under 30 minutes."

---

## **Getting Started**

### **Prerequisites**:
- Python 3.8+
- Required libraries (see `requirements.txt`)

### **Setup**:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/SHL_Assessment_Recommendation_System.git
   cd SHL_Assessment_Recommendation_System
