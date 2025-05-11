# Sentiment Analysis on Amazon Reviews

This project performs sentiment analysis on Amazon product reviews using Python (Jupiter Notebook). It includes data preprocessing, visualization, feature extraction, and classification using machine learning techniques.

## Project Structure

- **Notebook**: `Sentiment Analysis.ipynb`
- **Dataset**: `amazon_reviews.csv`

## Libraries Used 

- `pandas`, `matplotlib`, `seaborn` — for data manipulation and visualization.
- `nltk` — for text preprocessing and sentiment analysis.
- `scikit-learn` — for machine learning and evaluation.
- `wordcloud` — for visualizing frequent words shown in font size or color.
- `tqdm` — for progress bars.

## Workflow Summary

1. **Data Loading**
   - Reads in `amazon_reviews.csv` containing user-generated product reviews.

2. **Data Exploration**
   - Displays data info and performs exploratory data analysis.
  
3. **Data Cleaning**
   - Renaming unamed to userID.
   - Removing missing values using the dropna.

4. **Text Cleaning**
   - Applies regex-based cleaning and removes stopwords using NLTK.
   - Romoving special character such as punctuation marks from the text.
   - Reviewing text.

5. **Visualization**
   - Generates a word cloud of the most frequent words.

6. **Train-Test_Split**
   - Data were seprated into two sunsets to ensure that the model can be trained on one part (training set) and tested on another part (testing set).

7. **Feature Extraction**
   - TF-IDF vectorization was used to convert text into numeric features.
  
8. **Model Building**
   - Trains a Logistic Regression model to classify sentiments.
   - Applying SMOTE to balance the classes over_sample the minority class by creating.  synthetic samples to ensure a balance dataset.
   - GridSearchCV was used to look for the best logistic regression model for hyperparameter.
     
9. **Performance Model**
    The performance of the model was evaluated using:
   - Classification Report: which provides detailed metrics such as precision.
   - Confusion Matrix: this is to show how well the model predicted each class higlighting areas where the model made errors.
  
10. **VADER Sentiment Analysis**
   - Applies VADER from NLTK for rule-based sentiment scoring.

## How to Run
1. Clone or download the repository.
2. Ensure `amazon_reviews.csv` is in the same directory.
3. Run the notebook in Jupyter or any compatible environment.
4. Install dependencies using pip (if needed):
   ```bash
   pip install pandas matplotlib seaborn nltk scikit-learn wordcloud tqdm
   ```
## Output 
- Word clouds for sentiment visualization.
- Classification metrics for logistic regression.
- Receiver Oprating Characteristics (ROC)
- VADER sentiment scores.

## Notes
- Make sure to download NLTK stopwords and VADER lexicon:
  ```python
  import nltk
  nltk.download('stopwords')
  nltk.download('vader_lexicon')
  ```

      

   
