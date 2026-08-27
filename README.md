# Customer_Support_Dissertation-


# Author Name : Salva Muskan

# Project Overview
This project develops a Machine Learning system for classifying customer
support tweets into four categories: Complaint, Question, Positive, and
Other. The project evaluates multiple baseline and hyperparameter-tuned
classification models to identify the most effective approach for
customer support tweet classification.

The implemented workflow includes text preprocessing, feature extraction
using TF-IDF, baseline model evaluation, hyperparameter optimisation,
comparative performance analysis, SHAP explainability, prototype
development, and human evaluation functionality.

Problem Statement
Customer support organisations receive large volumes of social media
messages containing complaints, questions, positive feedback, and other
forms of communication. Manual classification can be time-consuming and
inconsistent. This project addresses this problem by developing and
evaluating Machine Learning models that automatically classify customer
support tweets into meaningful categories.

Dataset
The project uses a customer support tweet dataset containing labelled
textual messages. The dataset supports supervised multi-class
classification across the following categories:

Complaint

Question

Positive

Other

The textual data was prepared for Machine Learning modelling through
preprocessing and transformation into numerical features using TF-IDF.

Machine Learning Models
The following models were evaluated:

Logistic Regression

Random Forest

CatBoost

Multinomial Naïve Bayes

Each model was first evaluated using baseline settings and then assessed
after hyperparameter optimisation.

Evaluation Metrics
Model performance was evaluated using:

Accuracy

Precision

Recall

F1-Score

Macro F1-Score

ROC-AUC

Macro F1-Score was particularly useful for comparing overall performance
across the classification categories.

Baseline Model Results
The baseline evaluation produced the following results.

Model Accuracy Precision Recall F1-Score Macro ROC-AUC
F1-Score

Logistic 0.7344 0.7455 0.7344 0.7380 0.7379 0.9119
Regression

Random Forest 0.7603 0.7755 0.7603 0.7657 0.7655 0.9189

CatBoost 0.7817 0.7949 0.7817 0.7852 0.7850 0.9218

CatBoost achieved the strongest baseline performance across the major
evaluation metrics. It obtained an Accuracy of 0.7817, an F1-Score of
0.7852, a Macro F1-Score of 0.7850, and the highest ROC-AUC of 0.9218.
Random Forest produced the second strongest baseline performance, while
Logistic Regression also achieved competitive results. Multinomial Naïve
Bayes produced the lowest overall performance among the evaluated
baseline models.

Tuned Model Results
After hyperparameter optimisation, the models produced the following
results.

Model Accuracy Precision Recall F1-Score Macro ROC-AUC
F1-Score

Logistic 0.7481 0.7526 0.7481 0.7500 0.7498 0.9114
Regression

Random Forest 0.7649 0.7819 0.7649 0.7707 0.7706 0.9234

CatBoost 0.7664 0.7814 0.7664 0.7696 0.7695 0.9263

Hyperparameter optimisation improved several models. Random Forest
achieved the highest tuned Macro F1-Score of 0.7706 and the highest
tuned F1-Score of 0.7707. CatBoost achieved the highest tuned Accuracy
of 0.7664 and the strongest ROC-AUC of 0.9263. Logistic Regression also
improved after tuning, while Multinomial Naïve Bayes showed a smaller
improvement.

Baseline and Tuned Macro F1-Score Comparison
Model Baseline Macro F1-Score Tuned Macro F1-Score

Logistic Regression 0.7379 0.7498
Random Forest 0.7655 0.7706
CatBoost 0.7850 0.7695
Multinomial Naïve Bayes 0.6640 0.6674

The comparison demonstrates that hyperparameter optimisation did not
improve every model equally. Logistic Regression, Random Forest, and
Multinomial Naïve Bayes improved their Macro F1-Scores after tuning.
Random Forest became the strongest tuned model based on Macro F1-Score.
CatBoost remained the strongest baseline model but its Macro F1-Score
decreased slightly after tuning.

Best Performing Results
Two important findings emerged from the evaluation.

CatBoost was the best baseline model, achieving a Macro F1-Score of
0.7850.

Random Forest was the best tuned model based on Macro F1-Score,
achieving 0.7706.

CatBoost achieved the highest tuned ROC-AUC of 0.9263.

These findings show that model selection should consider multiple
evaluation metrics rather than relying on Accuracy alone.

SHAP Explainability Results
SHAP analysis was used to examine the influence of textual features on
model predictions. The SHAP feature importance results identified terms
including issue, problem, thanks, bad, thank, not, wrong, error, fix,
and issues as influential features.

The SHAP summary and decision plots demonstrated that different words
could positively or negatively influence the model output depending on
their presence and contribution to individual predictions. Terms such as
issue and problem showed particularly high feature importance,
supporting the interpretation of customer support classification
decisions.

The explainability analysis provides additional transparency by showing
how important textual features contribute to classification outcomes.

Prototype
A desktop prototype was developed for customer support tweet
classification. The prototype provides a Tweet Classification interface
where users can enter a customer support message and obtain a predicted
category and confidence value.

The prototype supports the four classification categories:

Complaint

Question

Positive

Other

The interface also displays prediction probabilities and provides
functions for prediction, clearing input, loading examples, and exiting
the application.

Example prototype results demonstrated successful classification of a
question with 87.08 percent confidence, an Other category prediction
with 43.01 percent confidence, and a complaint prediction with 88.80
percent confidence.

Human Evaluation
The prototype includes a Human Evaluation section designed to support
user assessment of the developed system. This component allows the
usability and practical relevance of the prototype to be considered
alongside quantitative Machine Learning evaluation.


Requirements
The project can be run using Python and the required Machine Learning
and data analysis libraries. Typical dependencies include:

Python

pandas

numpy

scikit-learn

CatBoost

SHAP

matplotlib

Running the Project
Clone or download the project files.

Install the required dependencies.

Prepare the dataset in the appropriate data directory.

Run the preprocessing and model training workflow.

Evaluate the baseline and tuned models.

Generate the explainability results.

Run the prototype application to classify customer support tweets.

Key Contributions
The project provides a comparative evaluation of four Machine Learning
algorithms for customer support tweet classification.

It evaluates both baseline and hyperparameter-tuned configurations.

It uses multiple performance metrics to support robust model comparison.

It identifies different best-performing models depending on the selected
evaluation metric.

It applies SHAP explainability to improve transparency and
interpretation.

It implements a functional prototype for practical tweet classification.

Conclusion
The project demonstrates that Machine Learning can support the automated
classification of customer support tweets into Complaint, Question,
Positive, and Other categories. The experimental results show strong
performance across several models, with CatBoost producing the strongest
baseline Macro F1-Score and Random Forest achieving the strongest tuned
Macro F1-Score. SHAP analysis improved the interpretability of the
classification process by identifying influential textual features. The
developed prototype translated the evaluated Machine Learning approach
into a practical application for customer support tweet classification
