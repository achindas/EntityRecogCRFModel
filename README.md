# Healthcare Entities Recognition - Syntactic Processing with CRF

## Table of Contents
* [NER & CRF Overview](#ner-and-crf-overview)
* [Problem Statement](#problem-statement)
* [Technologies Used](#technologies-used)
* [Approach for Modeling](#approach-for-modeling)
* [Classification Outcome](#classification-outcome)
* [Conclusion](#conclusion)
* [Acknowledgements](#acknowledgements)

## NER and CRF Overview

### Named Entity Recognition (NER)

NER is a fundamental task in **Natural Language Processing (NLP)** that involves identifying and classifying entities in text into predefined categories such as names of persons, organizations, locations, dates, diseases, treatments, and other domain-specific terms. NER is crucial in extracting structured information from unstructured text, enabling downstream applications like knowledge graph creation, question answering, and document classification. 

In the healthcare domain, NER can be employed to extract critical information like diseases, medications, treatments, and symptoms from medical texts.

### Conditional Random Fields (CRF)

CRF is a popular probabilistic model used for sequence labeling tasks like NER. CRF works by considering the **context of neighboring words** in a sequence, which allows it to model dependencies between words and their corresponding labels more effectively. In NER, CRF predicts the most probable sequence of entity labels (e.g., "Disease," "Treatment," or "O") by maximizing the conditional probability of the label sequence given the input text. 

By incorporating features such as `word embeddings, part-of-speech tags, and word shapes`, CRF ensures high precision and recall in entity recognition tasks, making it particularly effective for complex domains like healthcare, where capturing contextual relationships is essential.


## Problem Statement

A hypothetical health tech company called ‘BeHealthy’ aims to connect the medical communities with millions of patients across the country.

‘BeHealthy’ has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions.

So, ‘BeHealthy’ is providing medical services, prescriptions and online consultations and generating huge data day by day.

A part of this data are the prescriptions given by Doctors which includes statements regarding the patient's disease and prescribed treatments. We have been given such a data set in which a lot of text is provided related to the diseases of various patients and their related treatments implicitly.

But, the diseases and their treatment are not explicitly mentioned in the dataset. We have been asked to determine the disease name and its probable treatments from the dataset and list it out in the form of a table or a dictionary.

We need to build a custom NER (Name Entity Recognition) system using CRF-based (Conditional Random Field) solution to accomplish this task.

## Technologies Used

Python Jypyter Notebook in local PC environment has been used for the exercise. Apart from ususal Python libraries like  Numpy and Pandas, there are machine Learning specific libraries used to prepare, analyse, build model and visualise data. The following model specific libraries have been used in the case study:

- spaCy
- sklearn_crfsuite
- nltk


## Approach for Modeling

The following steps are followed to build the custom NER model for healthcare entities recognition:

1. Workspace Setup
2. Data Processing
3. Concept Identification
4. Definition & Extraction Functions for Features
5. Preparation of Input & Target Variables for Model
6. CRF Model Building
7. Evaluation of the Model
8. Diseases & Treatments Prediction
9. Conclusion

Some distinguishing processes in this approach include,

- Determining `Parts of Speech (PoS)` tags for all sentences and confirm that target entities predominantly belong to Noun & Proper Noun PoS

- Defining the `word features` including the features of previous and next words for input to CRF model

- Evaluating the model in terms of `F1 score`


## Classification Outcome

In this **Named Entity Recognition (NER)** exercise, we successfully developed a **Conditional Random Field (CRF)** model to extract medical entities, specifically `diseases` and their corresponding `treatments`, from a corpus of medical sentences. The model demonstrated very good performance, achieving an impressive **F1-score of 91.96%**, indicating high accuracy and robustness in entity recognition. This result underscores the effectiveness of CRF models in capturing contextual dependencies and patterns in sequential data, which is crucial for medical text processing. 

Such a system can significantly aid in automating medical information extraction, thereby facilitating advanced healthcare applications such as clinical decision support, electronic medical record analysis, and medical research.


## Conclusion

The success of this Named Entity Recognition (NER) exercise highlights the effectiveness of leveraging Conditional Random Field (CRF) models for extracting meaningful entities from complex text data. CRF models excel in capturing **contextual dependencies and structured relationships**, making them particularly suitable for tasks like identifying diseases and treatments in the healthcare domain. Beyond healthcare, NER systems powered by CRF modeling can be applied across various business domains, such as **finance** for extracting financial entities, **e-commerce** for product categorization, **legal** for document analysis etc.


## Acknowledgements

This case study has been developed as part of Post Graduate Diploma Program on Machine Learning and AI, offered jointly by Indian Institute of Information Technology, Bangalore (IIIT-B) and upGrad.