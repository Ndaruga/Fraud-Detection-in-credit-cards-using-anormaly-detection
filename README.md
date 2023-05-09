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

## Methods

The project uses two methods to detect fraud transactions:

- **Angle-based Outlier Detection (ABOD)**: This method measures the variance of the angle between each instance and its neighbors. The instances with higher variance are considered as outliers.

- **Autoencoders**: This method uses a neural network that learns to reconstruct its input by compressing it into a lower dimensional representation. The instances with higher reconstruction error are considered as outliers.

## Results

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
