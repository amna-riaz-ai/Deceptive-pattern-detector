# Deceptive Pattern Detector in E-Commerce

**Author:** Amna Riaz | Dalian Maritime University | MSc Artificial Intelligence

## Overview
This project automatically detects deceptive design patterns, also called dark 
patterns, in e-commerce website text using NLP and machine learning. Dark patterns 
manipulate consumers into unintended purchases, data sharing, or unwanted 
subscriptions through carefully crafted text like "Only 2 left!" or "Hurry! Sale 
ends soon!"

## Dataset
Real dark patterns dataset containing 2,426 labeled e-commerce text samples across 
multiple categories including Urgency, Scarcity, Social Proof, and Misdirection.

## Problem
Manually identifying deceptive patterns across millions of web pages is impossible. 
Most existing research focuses on visual UI analysis requiring screenshots and 
computer vision — making it heavy and slow for real time detection.

## Solution
A lightweight NLP pipeline using TF-IDF vectorization with bigrams to convert text 
into numerical features, SMOTE to handle class imbalance, and three ML models 
compared for best performance. Works purely on text making it fast and deployable 
as a real time browser extension or API.

## Results
| Model | Accuracy | F1 Score | AUC-ROC |
|---|---|---|---|
| Logistic Regression | 77.7% | 0.774 | 0.885 |
| Random Forest | 81.5% | 0.813 | 0.913 |
| XGBoost | 80.2% | 0.799 | 0.881 |

## Live Prediction Examples
| Text | Prediction | Confidence |
|---|---|---|
| Only 2 left in stock! Order now! | DECEPTIVE | 96.0% |
| FREE SHIPPING ON ORDERS OVER $50 | DECEPTIVE | 97.0% |
| LIMITED TIME OFFER! 80% OFF TODAY ONLY! | DECEPTIVE | 89.5% |
| Contact us for more information | NORMAL | 31.0% |

## Key Finding
Words like "review", "save", "share", and "member" are the strongest indicators 
of deceptive patterns in e-commerce text according to feature importance analysis.

## Technologies
Python, Scikit-learn, TF-IDF, Random Forest, XGBoost, SMOTE, Pandas, Matplotlib

## Real World Impact
Consumers can be protected in real time through browser extensions. Regulatory 
bodies can audit e-commerce platforms at scale. Businesses can self-audit their 
website copy for ethical design practices.
