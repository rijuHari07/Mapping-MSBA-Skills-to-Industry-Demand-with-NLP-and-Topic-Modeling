# Mapping-MSBA-Skills-to-Industry-Demand-with-NLP-and-Topic-Modeling

This project evaluates how closely leading MS in Business Analytics programs align with real world hiring needs for Data Analyst, Business Analyst, and Data Scientist roles. Using web scraped curriculum text and job posting text, it builds an end to end NLP workflow to measure skill overlap, surface gaps, and summarize themes employers emphasize most.

## Why this matters
MSBA programs often claim industry relevance, but course descriptions do not always reflect what job postings actually ask for. This analysis quantifies that match and highlights where technical coverage is strong and where it falls short.

## What this project does
- Collects MSBA course and program descriptions from top global universities
- Scrapes analytics job postings for Data Analyst, Business Analyst, and Data Scientist roles
- Cleans and standardizes text for fair comparisons
- Converts text into features using bag of words
- Measures curriculum to job similarity using cosine similarity
- Runs topic modeling (LDA) to identify major skill themes in job descriptions
- Compares topic coverage and skill gaps across programs
- Produces visual summaries to make the findings easy to interpret

## Workflow
### 1) Data collection
- Curriculum descriptions gathered from university program pages
- Job postings collected from Indeed for three role types
  - Data Analyst
  - Business Analyst
  - Data Scientist

### 2) Text preprocessing
Typical NLP cleaning steps were applied:
- Lowercasing
- Tokenization
- Stopword removal
- Lemmatization
- Regex based cleanup

### 3) Feature extraction and similarity scoring
- Bag of words features created using CountVectorizer
- Cosine similarity used to score overlap between curriculum language and job language
- Outputs include similarity comparisons by university and by role type

### 4) Topic modeling
- LDA topic modeling applied to job postings to uncover dominant skill clusters
- Topics often map to groups such as:
  - Machine learning
  - SQL and data engineering
  - Statistics
  - Cloud platforms
  - Business intelligence tools

### 5) Insights and visualization
Visualizations include:
- Similarity heatmaps for program versus job alignment
- Topic distribution comparisons across roles
- Skill gap views showing frequently requested job skills missing from curricula
- Word clouds or ranked keyword summaries for high demand skills

## Key findings
- Many programs show stronger alignment with business analysis oriented skills than data science specific skills
- Common gaps appear in machine learning depth, cloud tools, and NLP related skills
- Technical rigor varies widely across universities even when programs share similar titles

## Tech stack
- Python
- Pandas, NumPy
- scikit learn (CountVectorizer, cosine similarity, LDA)
- NLTK (stopwords, lemmatization)
- Gensim (topic modeling)
- Matplotlib, Seaborn
- Jupyter Notebook
   pip install -r requirements.txt

