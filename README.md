# Fake_News_Detection

### Background/business problem/introduction

In our project, we applied the machine learning technique of deep learning to detect fraudulent or false messages, also known as “fake news” on social media platforms. According to a 2019 [Pew](https://www.pewresearch.org/journalism/2019/06/05/many-americans-say-made-up-news-is-a-critical-problem-that-needs-to-be-fixed/) study, most Americans see made-up news as detrimental, negatively impacting trust in societal institutions, public health, and even democratic stability. 

We wanted to identify the fake news by only looking at the text - that is, without images or social network analysis. We built classification models using machine learning methods and aimed to improve the accuracy of the prediction of the models.

### Data sources
Data sources: For the source and more information about the datasets, please look at [Dataset Information.pdf](https://github.com/yufeifeiqiqi/Fake_News_Detection/blob/main/Dataset%20Information.pdf). 

You can download all data from https://drive.google.com/drive/folders/1kTtd8OqZdDjbWToHkFIwv37qroyx-4tj?usp=sharing. 

The starting point for this project was a 2019 codebase in Github which used 3 datasets to train their model:
- DATASET 1. Real news and fake, 20k rows, scraped from more than 240 websites 
- DATASET 2. All fake, 13k rows, scraped from 244 websites
- DATASET 3. All true, 38k rows

We sought to improve this model with an expanded data set and thus added one more:
- DATASET 4. TI_CNN, 20k rows only for testing



### Workflow
1. Start from a [reference project from GitHub](https://github.com/AIRLegend/fakenews) to build a solid foundation
2. Datasets were carefully collected from Kaggle and research papers
3. Cleaned the text and titles
4. Text tokenization, Vectorization, by finding vector representations using GoogleNews-vectors-negative300
5. Truncated and padded the text and title arrays to ensure uniform lengths
6. Label encoding: we used one-hot encoding, representing fake labels as 0 and true labels as 1
7. Train and test two different models (CNN, Bert)
8. Test models on the separate TI_CNN dataset to evaluate the generalization capability of our models. 


### Improvements from the GitHub reference project
- Used larger datasets by merging three distinct datasets for our training process
- Enhanced the quality of our data by lowering the text and translating emojis into their corresponding words!
- Remove stop words using the NLTK library
- We made the most out of Bayesian Optimization, leveraging its results to tune our models. Surprisingly, the GitHub group did not utilize these results, but we integrated them effectively.
- We also encountered some Bert Model codes from the GitHub group but noticed a lack of analyses and testing results. So, to ensure full control over our process, we decided to create the Bert Model from scratch.

### Models
- Can download the saved models used for this project:old_cnn_model.h5, new_cnn_model.h5, retrain_cnn_model.h5
from https://drive.google.com/drive/folders/1VkcKQqGNKT4T_wksyDOy_7rwAPujpQzY?usp=sharing











