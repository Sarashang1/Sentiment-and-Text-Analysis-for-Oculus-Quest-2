# Sentiment-and-Text-Analysis-for-Oculus-Quest-2
The data, content, and final delivery I shared on GitHub utilize mock-up data due to confidentiality. This work sample aims to demonstrate my analytical skills, problem-solving approach, and the lessons I learned from the case.

## Introduction:
At Brandeis International Business School, I undertook a project focused on the sentiment analysis of Oculus Quest 2 reviews. The overarching objective was to ensure Google's marketing and product teams derive actionable insights from genuine customer feedback.

## Objective:
The core objective of this project was threefold:
1. Acquisition of Authentic Feedback: To gather a comprehensive dataset of Oculus Quest 2 reviews from a reputable source, ensuring the integrity and reliability of the analysis.
2. Quantitative Analysis: To develop predictive models that gauge the sentiment of reviews, even those devoid of explicit ratings.
3. Qualitative Insights: To distill customer feedback into discernible themes and patterns, providing a clear roadmap for product enhancements and marketing strategy modifications.

## Model construction:
### 1. Data Acquisition and Preprocessing:

Web Scraping:
- Utilized Selenium in Python to extract reviews from bestbuy.com's Oculus review page.
Leveraged WebDriver, an essential tool for automating browser activities in conjunction with Selenium.
Designed an iterative scraping mechanism, collecting data such as raw HTML, review text, review date, and review star ratings, eventually accumulating a dataset of 5,054 reviews.

![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/2385bb7e-82c9-4c9a-9c69-32cccad8ef8a)

- Data Cleaning:
Addressed data challenges including missing values, duplicates, and inconsistencies in format.
Employed various Python libraries and tools to streamline and standardize the data for subsequent analysis.

Part of my data looks like:
![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/e5dd9906-4361-443d-a9a8-2ba9b68ea244)

### 2. Sentiment Analysis:

- Natural Language Processing (NLP) Techniques:
  - Applied noise reduction and cleaned review text by decomposing contractions, e.g., transforming 'n't' to 'not'.
  - Tokenized the text, effectively breaking it down into individual words or tokens.
  - Removed stop words like "the," "and," "is," etc., to declutter the data.
  - Used lemmatization to derive the base or root form of words, aiding in an accurate extraction of sentiment.

- Vectorization:
  - Adopted CountVectorizer to transmute text into vectors based on word frequency, with considerations for word pairings (bigrams) and triplets (trigrams).
    
- Data Splitting:
  - Segregated data into training (80%), validation (10%), and testing sets (10%).
  - Model Implementation and Evaluation:

- KNN Classifier:
  - Determined optimal value for 'k' using the elbow method.
  - Achieved an accuracy rate of 78%.

  ![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/4ea62950-2518-4c85-8362-246eb8778b11)

- Logistic Regression:
  - Adapted for multi-class classification.
  - Attained an accuracy of 86%.
    
![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/8619a712-f921-4150-bf6e-f27f7afdefe0)

### 3. Text Analysis:

- Review Categorization:
  - Segregated reviews into Neutral (3 stars), Positive (≥ 4 stars), and Negative (≤ 2 stars).

![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/c65bfc43-27f7-4033-9052-3c121d222358)

- Review Insights:
  - Average rating: 4.68/5.
  - Low-rating reviews comprised just 4% of the total, averaging 314 words in length.
  - Leveraged CountVectorizer to discern frequently mentioned terms and phrases across all rating categories.
    - Positive Feedback: Praise centered around the Oculus Quest 2's user-friendliness, suitability for all age groups, engaging VR experience, and extended battery life. The requisite Facebook account linkage was a notable point of contention.
 
      ![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/acfae4d9-2971-4d5f-8127-0d6356f23796)

    - Negative Feedback: The predominant grievance was the mandatory Facebook account. A handful of users desired greater clarity in the VR experience.
 
      ![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/f82235fb-3355-40f1-878e-8c5c7f639deb)

    - Overall: Overwhelmingly positive reception with commendations on its immersive gaming experience.

      ![image](https://github.com/Sarashang1/Sentiment-and-Text-Analysis-for-Oculus-Quest-2/assets/115900641/fcc55fb6-e0eb-4e2c-9326-f9870bc0d7ec)


## Reflections and Future Enhancements:

- Dataset Imbalance: The pronounced skewness in our dataset, with an overwhelming amount of positive reviews, presented challenges. In hindsight, it would have been beneficial to adopt techniques like oversampling or undersampling to create a more balanced dataset for training predictive models.

- Model Exploration: While the KNN and Logistic Regression models provided commendable accuracy rates, the incorporation of tree-based models or advanced neural networks in future projects might unearth deeper patterns and yield superior prediction accuracies.

- Feature Engineering: The project could further benefit from more advanced NLP techniques or the inclusion of additional features, perhaps drawing from metadata like review dates or user profiles.

## Conclusion:
Sentiment analysis, when deployed thoughtfully, can serve as a powerful lens through which companies perceive their product's reception in the market. In the case of Oculus Quest 2, this project not only affirmed its largely positive market reception but also spotlighted areas for potential enhancement – a testament to the utility of such endeavors.

However, the journey doesn't conclude with analysis. These insights must catalyze action. Be it refining product features in line with feedback or tailoring marketing strategies to accentuate strengths and address perceived weaknesses, the true value of sentiment analysis is realized in its translation to tangible improvements. The success of future Oculus iterations, and indeed any product, hinges on this dynamic interplay between customer feedback and product evolution.





