# Fraud-Detection-in-credit-cards-using-anormaly-detection
This project involves identifying unusual patterns or behaviors that may indicate fraudulent activity. Anomaly detection algorithms work by learning patterns from historical data and then detecting deviations from those patterns in new data.


## Dataset

The dataset contains transactions made by credit cards in September 2013 by European cardholders. The dataset is highly imbalanced, as only 0.172% of transactions are fraudulent. 

The dataset has been anonymized using Principal Component Analysis (PCA), and only contains numerical input variables which are the result of a PCA transformation. 

The only features which have not been transformed with PCA are 'Time' and 'Amount'. The feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

The dataset can be downloaded from [this link](https://github.com/Ndaruga/Fraud-Detection-in-credit-cards-using-anormaly-detection/blob/main/data.rar) or cloned with the repository.

## Requirements

This project does not have heavy procesing but you need the following resources to run it.
-   [Anaconda](https://docs.anaconda.com/free/anaconda/install/index.html) installation
-   Minimum 8 GB Ram
-   Alternatively, you can use [google colab](https://colab.google/) to run the file. Ensure you upload all the necessary files like `abod.py` and the `data.rar`

## Data Analysis Results
### Identifying Trends in Fraudulent Transactions
One of the first steps in fraud detection is to identify trends and patterns within fraudulent transactions. By analyzing a dataset containing transaction records, we can uncover insights that may reveal suspicious behavior. Let's take a look at some key findings from our analysis:

#### Top 10 Jobs with the Most Fraudulent Transactions
We discovered that certain professions are associated with a higher frequency of fraudulent transactions. Among the top 10 jobs with the most fraudulent transactions are Quantity Surveyors, Naval Architects, and Materials Engineers. 


These insights can help financial institutions target their fraud detection efforts more effectively.

#### Credit Card Holders with the Most Fraudulent Transactions
Moreover, we examined the credit card holders who were involved in the most fraudulent transactions. Interestingly, some credit card numbers appeared more frequently in fraudulent activities than others. By identifying these patterns, financial institutions can implement measures to prevent fraudulent activities associated with specific credit cards.

#### Hourly Analysis of Fraud Transactions
We also analyzed the hourly distribution of fraudulent transactions to identify any temporal patterns. This analysis revealed that fraudulent activities tend to peak during certain hours of the day, providing valuable insights for deploying real-time fraud detection systems.

### Machine Learning for Fraud Detection
Another crucial aspect of fraud detection is the application of machine learning algorithms. By training models on historical transaction data, we can develop predictive models that identify potentially fraudulent transactions in real-time. Here's a glimpse into our machine learning pipeline:

#### Feature Engineering and Encoding
We preprocessed the dataset by encoding categorical variables and performing feature engineering to extract relevant information for training our machine learning models.

#### Training and Evaluation
We split the data into training and testing sets, trained several machine learning models, and evaluated their performance using metrics such as precision, recall, and F1-score.

### Machine learning Methods

The project uses two methods to detect fraud transactions:

- **Angle-based Outlier Detection (ABOD)**: This method measures the variance of the angle between each instance and its neighbors. The instances with higher variance are considered as outliers.

- **Autoencoders**: This method uses a neural network that learns to reconstruct its input by compressing it into a lower dimensional representation. The instances with higher reconstruction error are considered as outliers.

### Results

The project evaluates the performance of the methods using metrics such as accuracy, precision, recall, and f1-score. The results are shown in the following table:

| Method | Accuracy | Precision | Recall | F1-score |
|--------|----------|-----------|--------|----------|
| ABOD   | 0.991    | 0.042     | 0.802  | 0.080    |
| Autoencoders | 0.994 | 0.813 | 0.796 | 0.804 |

## How to run

To run this project, you need to follow these steps:

- Clone this repository to your local machine
- Unzip the dataset in the same folder as the repository
- Open the Jupyter notebook `Fraud_detection_in_credit_cards.ipynb` and run the cells
- You can also run the Python script `abod.py` to apply the ABOD method separately

## License

This project is licensed under the MIT License - see the LICENSE file for details.
