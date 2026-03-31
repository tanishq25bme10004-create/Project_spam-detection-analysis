### **Spam Detection Algorithm Comparison Study (CSA2001)**

### 

###  Project Information



##### \- Course: Fundamentals of AI and ML

##### \- Student Name: Tanishq Loharuka

##### \- Registration Number: 25BME10004

##### \- Institution: Vellore Institute of Technology Bhopal (VIT - BHOPAL)







1. ## **Problem Statement**



Spam messages constitute a significant challenge in modern digital communication, wasting users' time, posing security risks through phishing attempts, and cluttering important communication channels. Manual spam filtering is impractical given the volume of messages sent daily, necessitating automated machine learning solutions.



\*\*Research Question\*\*: Which machine learning classification algorithms are most effective for spam detection, and what are the trade-offs between different approaches?



---



\## 2. Objectives



1\. Compare three machine learning algorithms (Naive Bayes, Logistic Regression, Random Forest) for spam classification

2\. Analyze the theoretical foundations of each algorithm

3\. Evaluate performance using multiple metrics (accuracy, precision, recall, F1-score, AUC-ROC)

4\. Provide evidence-based recommendations for spam detection systems



---



\## 3. Functional Requirements



\### Module 1: Data Loading and Preprocessing

\- Load SMS Spam Collection dataset (5,574 messages)

\- Clean and normalize text (lowercase, remove special characters)

\- Split data into training (80%) and testing (20%) sets with stratification



\### Module 2: Feature Extraction

\- Implement Bag-of-Words (BoW) vectorization

\- Implement TF-IDF vectorization with 3000 features

\- Compare feature extraction methods



\### Module 3: Algorithm Implementation and Training

\- Train Naive Bayes classifier (MultinomialNB)

\- Train Logistic Regression with regularization

\- Train Random Forest ensemble (100 trees)



---



\## 4. Non-Functional Requirements



1\. \*\*Performance\*\*: Model training should complete within 5 minutes on standard laptop hardware

2\. \*\*Accuracy\*\*: Target minimum 95% accuracy on test set for at least one algorithm

3\. \*\*Reproducibility\*\*: Set random\_state=42 for consistent results across runs

4\. \*\*Usability\*\*: Clear visualization of results with labeled charts and comparison tables

5\. \*\*Scalability\*\*: Design handles datasets up to 100,000 messages efficiently



---



\## 5. Technologies and Tools Used



\- \*\*Programming Language\*\*: Python 3.9+

\- \*\*Machine Learning\*\*: scikit-learn 1.3.0

\- \*\*Data Processing\*\*: pandas 2.0.0, numpy 1.24.0

\- \*\*Visualization\*\*: matplotlib 3.7.0, seaborn 0.12.0

\- \*\*NLP Tools\*\*: nltk 3.8.0

\- \*\*Development Environment\*\*: Google Colab

\- \*\*Version Control\*\*: Git, GitHub



---



\## 6. System Architecture



\### High-Level Architecture



Input (SMS Messages)

↓

Data Preprocessing

↓

Feature Extraction (TF-IDF)

↓

Train-Test Split

↓

Model Training (3 Algorithms)

↓

Performance Evaluation

↓

Results \& Visualizations







\### Data Flow

1\. Raw SMS messages loaded from dataset

2\. Text cleaned and normalized

3\. Features extracted using TF-IDF vectorization

4\. Data split into training and testing sets

5\. Three models trained independently

6\. Predictions made on test set

7\. Performance metrics calculated

8\. Results visualized and compared



---



\## 7. Implementation Details



\### Dataset

\- \*\*Source\*\*: SMS Spam Collection from UCI ML Repository

\- \*\*Size\*\*: 5,574 messages

\- \*\*Labels\*\*: Spam (747), Ham (4,827)

\- \*\*Format\*\*: Tab-separated text file



\### Preprocessing Pipeline





Text cleaning

text.lower() → remove special chars → normalize whitespace





\### Feature Extraction

\- \*\*TF-IDF Parameters\*\*: max\_features=3000, min\_df=2, max\_df=0.8

\- \*\*Vocabulary\*\*: Top 3000 most significant words



\### Model Parameters

\- \*\*Naive Bayes\*\*: alpha=1.0 (Laplace smoothing)

\- \*\*Logistic Regression\*\*: C=1.0, max\_iter=1000, solver='lbfgs'

\- \*\*Random Forest\*\*: n\_estimators=100, random\_state=42



---



## \## 8. Results



\### Performance Comparison



| Algorithm | Accuracy | Precision | Recall | F1-Score | AUC-ROC |

|-----------|----------|-----------|--------|----------|---------|

| Naive Bayes | 98.21% | 97.50% | 94.32% | 95.88% | 0.991 |

| Logistic Regression | 96.77% | 95.18% | 93.12% | 94.14% | 0.982 |

| Random Forest | 97.49% | 96.81% | 92.71% | 94.71% | 0.987 |



\### Training Time Comparison



| Algorithm | Training Time |

|-----------|---------------|

| Naive Bayes | 0.52s |

| Logistic Regression | 3.16s |

| Random Forest | 45.23s |



\*\*Analysis\*\*: Naive Bayes is 6x faster than Logistic Regression and 87x faster than Random Forest, making it ideal for real-time applications.







#### \*\*Winner:\*\* Naive Bayes with 98.21% accuracy and 95.88% F1-score









## \### Key Findings



1\. \*\*Naive Bayes achieved the highest accuracy of 98.21%\*\*, outperforming both Logistic Regression (96.77%) and Random Forest (97.49%)



2\. \*\*All algorithms exceeded the 95% accuracy threshold\*\*, demonstrating that spam detection is well-suited for machine learning approaches



3\. \*\*TF-IDF features were used exclusively\*\* and proved effective with vocabulary size of 3000 words



4\. \*\*Naive Bayes demonstrated the fastest training time\*\* at 0.5 seconds, compared to Logistic Regression (3.2s) and Random Forest (45.3s)



5\. \*\*Low false negative rates\*\* of 5.68% (Naive Bayes), 6.88% (Logistic Regression), and 7.29% (Random Forest) ensure effective spam catching



6\. \*\*Naive Bayes offers the best speed-accuracy tradeoff\*\* for real-time spam filtering applications











\### Visualizations



Generated visualizations include:

\- Confusion matrices for all three algorithms

\- ROC curves comparison

\- Performance metrics bar chart

\- Word importance analysis (Logistic Regression)



---



\## 9. Installation and Usage



\### Prerequisites



pip install scikit-learn pandas matplotlib seaborn nltk numpy





\### Running the Project



\*\*Step 1: Clone Repository\*\*





git clone \[your-repo-url]

cd spam-detection-analysis







\*\*Step 2: Run Notebooks in Order\*\*

1\. `01\\\\\\\_data\\\\\\\_exploration.ipynb` - Explore dataset characteristics

2\. `02\\\\\\\_preprocessing\\\\\\\_and\\\\\\\_features.ipynb` - Clean text and extract features

3\. `03\\\\\\\_model\\\\\\\_training\\\\\\\_and\\\\\\\_evaluation.ipynb` - Train models and evaluate



\*\*Step 3: View Results\*\*

\- Check `results/` folder for visualizations

\- Review `algorithm\\\\\\\_comparison\\\\\\\_results.csv` for metrics



---



\## 10. Testing Approach



\### Testing Strategy

\- \*\*Train-Test Split\*\*: 80-20 split with stratification to maintain class balance

\- \*\*Cross-Validation\*\*: 5-fold CV for robust performance estimation

\- \*\*Metrics\*\*: Multiple evaluation metrics to assess different aspects

  - Accuracy: Overall correctness

  - Precision: Reliability of spam predictions

  - Recall: Spam detection rate

  - F1-Score: Balanced metric



\### Test Cases

1\. \*\*High Confidence Spam\*\*: Messages with obvious spam indicators

2\. \*\*Borderline Cases\*\*: Messages that could be spam or ham

3\. \*\*Edge Cases\*\*: Very short messages, all caps, numbers only

4\. \*\*Ham Messages\*\*: Legitimate messages should not be flagged



---



\## 11. Challenges Faced



1\. \*\*Class Imbalance\*\*: Dataset has 86.6% ham, 13.4% spam

   - \*\*Solution\*\*: Used stratified splitting to maintain ratio in train/test



2\. \*\*Feature Selection\*\*: Choosing optimal vocabulary size

   - \*\*Solution\*\*: Tested different values, settled on 3000 features



3\. \*\*Stopword Handling\*\*: Deciding whether to remove stopwords

   - \*\*Solution\*\*: Compared both approaches, kept stopwords for better performance



4\. \*\*Model Comparison\*\*: Ensuring fair comparison across algorithms

   - \*\*Solution\*\*: Used same preprocessed data and evaluation metrics for all



---



\## 12. Learnings and Key Takeaways



\### Technical Learnings

1\. \*\*Text Preprocessing\*\*: Proper cleaning significantly impacts model performance

2\. \*\*Feature Engineering\*\*: TF-IDF captures word importance better than simple counts

3\. \*\*Algorithm Selection\*\*: Naive Bayes excels for text classification tasks

4\. \*\*Evaluation\*\*: Multiple metrics needed for comprehensive assessment



\### Conceptual Understanding

1\. Probabilistic vs. linear vs. ensemble approaches have different strengths

2\. Speed-accuracy tradeoffs are important for real-world deployment

3\. False positives vs. false negatives have different business impacts

4\. Cross-validation provides more reliable performance estimates



\### Best Practices

1\. Always split data before any processing to prevent data leakage

2\. Use stratification to handle imbalanced datasets

3\. Document all hyperparameters for reproducibility

4\. Visualize results for better interpretation









\### Error Analysis



\*\*Naive Bayes Confusion Matrix:\*\*

\- True Negatives: 963 (ham correctly identified)

\- False Positives: 4 (ham incorrectly marked as spam)

\- False Negatives: 16 (spam that slipped through)

\- True Positives: 132 (spam correctly caught)



\*\*Impact:\*\*

\- False Positive Rate: 0.41% (very low user inconvenience)

\- False Negative Rate: 10.8% (acceptable for spam filtering)





---



\## 13. Future Enhancements



1\. \*\*Deep Learning Models\*\*

   - Implement LSTM networks for sequential processing

   - Use BERT for contextual understanding



2\. \*\*Real-Time Deployment\*\*

   - Create REST API for spam detection service

   - Deploy model as microservice



3\. \*\*Advanced Features\*\*

   - Multi-language support

   - Sender reputation analysis

   - URL and attachment scanning



4\. \*\*Model Improvements\*\*

   - Hyperparameter tuning with GridSearchCV

   - Ensemble all three models

   - Implement online learning for adaptation



---



\## 14. References



1\. Almeida, T.A., Hidalgo, J.M.G. (2012). "SMS Spam Collection v.1" UCI Machine Learning Repository

2\. Manning, C.D., et al. (2008). "Introduction to Information Retrieval"

3\. scikit-learn Documentation: https://scikit-learn.org/

4\. NLTK Documentation: https://www.nltk.org/

5\. Pedregosa, F., et al. (2011). "Scikit-learn: Machine Learning in Python"



---



\## 15. Repository Structure



spam-detection-analysis/

├── README.md # This file

├── statement.md # Detailed problem statement

├── requirements.txt # Python dependencies

├── notebooks/

│ ├── 01\_data\_exploration.ipynb

│ ├── 02\_preprocessing\_and\_features.ipynb

│ └── 03\_model\_training\_and\_evaluation.ipynb

├── results/

│ ├── confusion\_matrices\_all\_algorithms.png

│ ├── roc\_curves\_all\_algorithms.png

│ ├── metrics\_comparison\_all\_algorithms.png

│ └── algorithm\_comparison\_results.csv

└── docs/

└── project\_report.pdf







\## Author



\*\*\[Altamash]\*\*

\- Registration Number: \[25BME10004]

\- Course: Fundamentals of AI and ML

\- Institution: VIT BHOPAL

\- Email: \[tanishq.25bme10004@vitbhopal.ac.in]

\- GitHub: \[https://github.com/tanishq25bme10004-create/Project_spam-detection-analysis]



---



\## License



This project is submitted as part of academic coursework at VIT and is for educational purposes only.







\*\*Last Updated\*\*: March 2026

