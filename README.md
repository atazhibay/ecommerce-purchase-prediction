# 🛍️ E-commerce Purchase Prediction

## 📑 Overview

This project focuses on predicting whether a user will purchase a product on an e-commerce platform, based on behavior such as views, cart additions, discount levels, and product attributes.

## 🧠 Features

| Feature               | Description                                                        |
|------------------------|--------------------------------------------------------------------|
| `category`             | Product category (Books, Electronics, etc.)                       |
| `price`                | Product price                                                     |
| `discount`             | Discount level (0 to 0.5)                                         |
| `views`                | Number of times a product was viewed                              |
| `cart_adds`            | How many times the product was added to cart                      |
| `rating`               | Product rating (2.5 to 5.0)                                       |
| `device`               | User device: Mobile / Desktop / Tablet                           |
| `purchased`            | Target: 1 — purchased, 0 — not purchased                          |
| `view_to_cart_ratio`   | Engineered feature: cart adds divided by views                   |
| `price_discounted`     | Engineered feature: final price after discount                   |
| `expensive`            | Flag for price > 700                                              |
| `is_mobile`            | Flag for mobile device                                            |

## 📊 Model Results

| Model               | F1-score | ROC AUC |
|---------------------|----------|---------|
| Logistic Regression | **0.321** | 0.703   |
| Random Forest       | 0.144    | **0.714** |

- **ROC AUC ≈ 0.70** indicates the model distinguishes between buyers and non-buyers better than random.
- **F1-score** shows model captures 1 out of 3 purchases correctly, which is acceptable under class imbalance.

## 📈 Visualizations

- ROC Curve for evaluating classification quality
- Confusion Matrix to visualize true/false positives and negatives

## 📦 Tools Used

- Python, pandas, scikit-learn, xgboost, lightgbm, matplotlib, seaborn
- SMOTE for handling class imbalance

## 🚀 How to Run

1. Clone the repository
2. Install requirements: `pip install -r requirements.txt`
3. Run `e-com.ipynb` notebook

## 🧾 License

MIT License
