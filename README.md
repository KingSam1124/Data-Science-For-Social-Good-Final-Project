Understanding Misinformation: A Case Study of COVID-19 Social Media Posts

Introduction: 

On March 11, 2020, the World Health Organization (WHO) officially declared
COVID-19 a global pandemic. Just a little over three years later, on May 5th, this global health
emergency ended. Unfortunately, throughout this period, the pandemic not only posed a
significant public health challenge to the world but also gave rise to widespread misinformation
on social media platforms. According to Pew Research Center (2021), nearly half of Americans
reported obtaining either ‘some’ (30%) or ‘a lot’ (18%) of news and information about COVID-19
vaccines from online sources. While this statistic may not appear as significant, such
information can lead to rumors, stigma, discrimination, and false theories, ultimately creating
confusion that restricts individual and public health responses during times of crisis. 

Background: 

In response to this growing issue, numerous researchers have developed models
aimed at detecting and mitigating the spread of false information. Murugesan et. al (2022), for
example, utilizes machine learning techniques like Adaboost & Decision tree algorithm to
identify fake news in the medical domain. Similarly, Farhoudinia et. al (2024) looked into using
sentiment analysis on a COVID-19 Twitter dataset to detect fake news. While these research
papers have offered valuable insights, there is still a research gap in combining all detection
methods together to identify the most significant features contributing to misinformation
classification.

Research Question: 

Which social media features are most important for distinguishing real vs
misinformation posts?

Data: 

The Fighting an Infodemic: COVID-19 Fake News Dataset (Patwa et al., 2021) consists of
10,700 English-language social media posts related to the COVID-19 pandemic. The content
was gathered from Twitter, Facebook, and Instagram using web scraping and the Twitter API.
Real news posts were collected from trusted organizations, including the World Health
Organization (WHO), the Centers for Disease Control and Prevention (CDC), and Covid India
Seva. In contrast, fake news posts were gathered from misinformation posts on social media.
The authors included 5,600 real news posts and 5,100 fake news posts to ensure a balanced
dataset. The dataset contains three columns: a numeric index, the text of the post, and a binary
label indicating whether the post is classified as “real” or “fake.” The research team 
manually verified each post to ensure accurate labeling.

Method: 

We want to identify the most influential factors for detecting misinformation in tweets
using feature engineering and machine learning. For each individual tweet we will extract a set
of key features, including tweet length, hashtag count, link presence, emotion, assigned using
the DisTilBERT model, sentiment polarity, which will have the levels positive, negative, or
neutral, and important words identified through TF-IDF weighting. These features are then used
two to train a Random Forest classification model. The dataset will be split into training and testing
sets to evaluate the model’s performance, making sure that it generalizes well to unseen data.
We selected the Random Forest algorithm because it is robust to overfitting, can handle a mix of
categorical and numerical features, and provides interpretable feature importance metrics.
Random Forest was especially attractive for this project because of its interpretability. This
makes it ideal for our goal of not only classifying tweets as real or fake, but also understanding
which tweet characteristics are most predictive of misinformation. The model's output will help
us pinpoint patterns in tweet content and structure that correlate strongly with authenticity,
providing both predictive power and actionable insights.
