# Sentiment Analysis Using LSTM Model

## Introduction
The primary objective of this project is to perform sentiment analysis on a dataset containing customer reviews. Sentiment analysis aims to categorize these reviews into positive, negative, or neutral sentiments. The process involves data preprocessing, building a Long Short-Term Memory (LSTM) model, and evaluating its performance.

## Requirements
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- tensorflow
- 
## Project Structure
1. **Data Loading and Initial Exploration**
    - **Dataset Loading**: The dataset is loaded from a CSV file named `new_data.csv` into a pandas DataFrame.
    - **Data Visualization**:
        - **Rating Distribution**: A histogram is plotted to show the distribution of ratings in the dataset.
        - **Sentiment Proportion**: A pie chart is used to display the proportion of different sentiments.
        - **Distribution of Ratings by Sentiment**: A bar chart shows the count of ratings for each sentiment category.

2. **Data Preprocessing**
    - **Sentiment Labeling**: Sentiments are converted to numerical values: Positive (1), Negative (-1), and Neutral (0).
    - **Text Cleaning**: The reviews are cleaned by converting to lowercase and removing punctuation.

3. **Train-Test Split**
    - The dataset is split into training and test sets with an 80-20 split.

4. **Tokenization and Padding**
    - **Tokenization**: The text data is tokenized and converted to sequences of integers.
    - **Padding**: Sequences are padded to ensure uniform length.

5. **Model Building**
    - **Model Architecture**: The LSTM model is built with the following layers:
        - Embedding Layer
        - LSTM Layer with 128 units (return_sequences=True)
        - Dropout Layer
        - LSTM Layer with 64 units
        - Dropout Layer
        - Dense Layer with softmax activation
    - **Compilation**: The model is compiled with Adam optimizer and categorical cross-entropy loss.
    - **Model Training**: The model is trained for 20 epochs.

6. **Model Evaluation**
    - **Performance Metrics**: The model's performance is evaluated using loss, accuracy, recall, F1 score, and AUC.
    - **ROC AUC Score**: The ROC AUC score for the multi-class classification is calculated.
    - **ROC Curve Plotting**: ROC curves for each class are plotted.

7. **Results**
    - **Test Metrics**: The model achieved the following metrics on the test set:
        - ROC AUC Score: The overall ROC AUC score for the multi-class classification was 

8. **Conclusion**
    - The LSTM model demonstrated reasonable performance in classifying sentiments of customer reviews. The accuracy, recall, and AUC scores suggest that the model is fairly effective in distinguishing between positive, negative, and neutral sentiments.
