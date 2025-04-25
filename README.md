# Job_Recommender_system
## **1. Introduction**  
This project aims to develop a comprehensive job recommendation system using a combination of **content-based filtering**, **classification**, and **ranking models**. It leverages machine learning and NLP to match job seekers with relevant opportunities based on their profiles and preferences.

### **1.1 Task Overview**  
Build a system that:
- Extracts and understands user résumé and job listing information using NLP.
- Classifies jobs and candidates based on domain and seniority.
- Recommends and ranks jobs tailored to the user profile.

### **1.2 Objectives**
- Extract meaningful features from both users and job listings.
- Classify users and jobs into job families using supervised learning.
- Recommend top-N job listings using similarity and ranking models.
- Evaluate system performance using F1-score and Mean Average Precision (MAP).

---

## **2. Project Initialization and Planning Phase**

### **2.1 Problem Statement**  
Job seekers often find it difficult to navigate through thousands of job listings to find the most suitable positions. Recruiters, too, struggle to find candidates that closely match job requirements. There is a need for a system that automates and personalizes this process.

### **2.2 Project Proposal (Proposed Solution)**  
Develop an ML-based recommender system that:
- Uses NLP to extract structured data from unstructured résumés and job descriptions.
- Classifies candidates and jobs into relevant categories.
- Scores and ranks job listings based on relevance to the user profile.

### **2.3 Initial Project Planning**  
- **Platform**: Google Colab  
- **Language**: Python  
- **Libraries**: pandas, scikit-learn, NLTK, spaCy, sklearn, matplotlib  
- **Data Format**: CSV files uploaded to Google Drive  
- **Modeling Approach**: TF-IDF + Cosine Similarity + Classification + Ranking  

---

## **3. Data Collection and Preprocessing Phase**  
- **Job Dataset**: 50 job listings with columns: job title, description, required skills.  
- **User Dataset**: 50 users with user name, skillset, education, work experience, job like history.  
- **Preprocessing Steps**:
  - Clean and tokenize text.
  - Use TF-IDF to vectorize profiles and job descriptions.
  - Normalize skillsets and descriptions.
  - Convert job family and seniority into labels using rule-based heuristics.

---

## **4. Model Development Phase**

### **4.1 Model Selection Report**
- **For Classification**: Random Forest, SVM  
- **For Recommendation**: Content-based filtering (TF-IDF + Cosine Similarity)  
- **For Ranking**: Relevance score based on similarity + classification category match  

### **4.2 Initial Model Training Code, Model Validation and Evaluation Report**
- Train classifier on labeled job/user family (e.g., `DataSci`, `Marketing`, etc.).
- Compute F1-score on classification labels.
- Compute Mean Average Precision (MAP) on top-N recommended jobs.
- Validate ranking by comparing predicted job families vs. liked job families.

---

## **5. Final Model Selection Justification**  
The Random Forest model achieved the highest F1-score with consistent predictions across user profiles. Combined with a hybrid content-based recommender, the system provided relevant recommendations with high MAP scores. TF-IDF was chosen for its lightweight nature and strong baseline performance.

---

## **6. Conclusion**  
The project successfully built a scalable job recommendation system that personalizes job listings based on a user's skillset, experience, and interest history. The system is modular and can be extended to include collaborative filtering or real-time recommendation pipelines.


---

## **9. Google Colab Link**

- **Google Colab Notebook**: [\https://colab.research.google.com/drive/1JDz0Nqsj9G10Wxq1e0AhnmbXze3PjDzn?usp=sharing]  
