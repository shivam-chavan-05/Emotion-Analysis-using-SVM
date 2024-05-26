# Emotion Analysis using  K-Means

### Introduction
In this report, I will present the
methodology, results, and insights garnered
from exploring emotion recognition in SVM for
pattern discovery. Through hands-on
experimentation SVM, I aimed to grasp
the intricacies of these method in analyzing
and interpreting textual data. This endeavor
provided valuable insights into the
application of machine learning algorithms
for emotion analysis and enhanced my
proficiency in NLP techniques.

### Data Preparation
#### Data loading
Upon receiving the dataset, it was provided
in a compressed .gz format. After extraction,
I discovered that the dataset was structured
as .json files. To streamline the data for
analysis, I opted to convert these files into
.csv format. This process ensured that the
data was in a more accessible and
standardized form for further exploration
and preprocessing.

![Image1](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/26f6f99b-04cc-41f5-9c7e-49e25c69c111)

#### Preprocessing
During preprocessing, I tokenized the text to
individual words, converted it to lowercase
for consistency, removed stop words, and
eliminated special characters. I also
lemmatized the words to normalize them
and added a new column with preprocessed
text. These steps improved data quality for
subsequent analysis and modeling.

![Image2](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/3ef3e75e-b9bf-421a-a89b-22db401474bf)


#### Feature Transformation
Finally, I transformed the text into numerical
representations using TF-IDF. This method
calculates the importance of each word in a
document relative to a corpus, helping to
capture the significance of words in the
dataset. TF-IDF conversion enabled the text
data to be effectively utilized for machine
learning algorithm such as
SVM.

![Image3](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/243c493a-c5ee-43a3-92f8-a8f470ce1441)


### SVM for Emotion Classification
#### Model Implementation
I employed the Support Vector Machines
(SVM) algorithm for emotion classification.
Utilizing the SVC class from the
sklearn.svm module, I initialized an SVM
classifier with default hyperparameters.
After training the classifier on the
preprocessed training data, predictions were
made on the test data. Accuracy and
classification reports were computed using
accuracy_score and classification_report
functions from sklearn.metrics. The
classification report shows varied precision,
recall, and F1-score for different emotions.

![Image1](https://github.com/shivam-chavan-05/Emotion-Analysis-using-SVM/assets/144063863/899d0ac3-0818-4b11-9531-96162d5b6a92)


I conducted grid search optimization for the
SVM classifier using GridSearchCV from
sklearn.model_selection, exploring various
kernel types, regularization parameters, and
gamma values. Despite finding the best
hyperparameters and initializing a new
classifier with optimized settings, the
accuracy and classification report remained
unchanged from the default SVM classifier.


![Image2](https://github.com/shivam-chavan-05/Emotion-Analysis-using-SVM/assets/144063863/972dd05f-579d-4fed-994c-7cecfff8042f)


#### Validation
I assessed the classifier's performance via
cross validation using
sklearn.model_selection's cross_val_score
and cross_val_predict functions. This
provided an average accuracy of around
49.88%, indicating consistent performance
across folds. The resulting classification
report showed similar trends to the initial
classification, with certain emotions
consistently exhibiting lower performance
metrics, notably 'anger', 'disgust', 'fear', and
'sadness'.


![Image3](https://github.com/shivam-chavan-05/Emotion-Analysis-using-SVM/assets/144063863/af469cce-b86f-467c-ba8a-e4fe9748e956)


### Model Insights
#### Performance Analysis

In the scenario without optimization, the
SVM classifier achieved an accuracy of
approximately 50.17%. The classification
report revealed varying precision, recall, and
F1-scores across different emotions.
Notably, emotions like 'anger', 'disgust',
'fear', and 'sadness' exhibited low precision
and recall, indicating the classifier's
difficulty in accurately predicting these
emotions.

![Image 4](https://github.com/shivam-chavan-05/Emotion-Analysis-using-SVM/assets/144063863/fdcfe890-c8e0-448f-8a93-51f3af867592)


Upon optimization with grid search, the
hyperparameters were tuned, but the
accuracy and classification report remained
unchanged from the default classifier. This
suggests that the default hyperparameters
already resulted in an optimal performance
level.

![Image5](https://github.com/shivam-chavan-05/Emotion-Analysis-using-SVM/assets/144063863/f9667f57-3a3e-4b21-b666-f4a7a9f46500)


Cross-validation further confirmed the
consistency of the classifier's performance,
with an average accuracy of approximately
49.49%. The classification report from
cross-validation exhibited similar trends as
the initial classification, indicating
robustness across different folds of the
training data.

![I,age6](https://github.com/shivam-chavan-05/Emotion-Analysis-using-SVM/assets/144063863/cbd5b1d3-2c8b-417d-b4e9-6aba4cc08af9)


#### Comparative Analysis
SVM focuses on precise emotion
classification with predefined labels,
providing detailed performance metrics. In
contrast, K-Means explores the dataset's
structure without labels, revealing broader
patterns and clusters of emotional content.
SVM emphasizes classification accuracy,
while K-Means emphasizes data exploration
and pattern identification.

### Insights and Applications
Through SVM classification and K-Means
clustering, I gained insights into the
multifaceted nature of human emotions,
shedding light on their complexity within
textual data. These findings have significant
implications for fields such as psychology,
sociology, and communication studies,
emphasizing the need for nuanced
approaches in understanding human
emotions and communication dynamics.
The insights garnered from SVM
classification and K-Means clustering offer
practical applications across various
domains. In marketing, sentiment analysis
aids in crafting targeted campaigns, while in
customer service, emotion analysis enhances
feedback interpretation for improved
services. Moreover, in healthcare, emotion
monitoring supports mental health
interventions, and in content moderation, it
contributes to creating safer online
environments.
