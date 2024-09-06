# Unraveling Emotional Well-Being through Social Media Analytics Using Deep Learning Algorithms

## Overview
The primary objective of this project is to understand the relationship between social media usage and the emotional well-being of users. Social media has become an integral part of daily life for many people, yet its impact on emotional well-being remains a controversial and complex topic. Some studies suggest that social media can have positive effects, such as enhancing social connections and providing access to information. However, other research highlights negative effects, such as increased feelings of anxiety, depression, and social isolation.

## Business Understanding
The challenge lies in analyzing the available data from various social media platforms to identify trends that may influence users' emotional well-being. This involves collecting and processing data from multiple sources, including posts, comments, and user activities, and linking them to emotional well-being indicators such as levels of happiness, anxiety, and life satisfaction.

To achieve this goal, it is necessary to develop and train analytical models capable of identifying and predicting the relationship between social media activity and changes in emotional well-being. These models are expected to assist researchers, policymakers, and individual users in better understanding the impact of social media on mental health, as well as in developing more effective strategies to minimize negative effects and maximize the positive benefits of social media usage.

## Data Understanding
This dataset provides valuable insights into social media usage and the dominant emotional states of users based on their activity. The dataset is ideal for exploring the relationship between social media usage patterns and emotional well-being. There are three files included in this dataset:

- `train.csv`: Data used for training the model.
- `test.csv`: Data used for testing the model.
- `val.csv`: Data used for validation purposes.

### Columns in the Dataset:
- **User_ID**: A unique identifier for each user.
- **Age**: The age of the user.
- **Gender**: The user's gender (Female, Male, Non-binary).
- **Platform**: The social media platform used (e.g., Instagram, Twitter, Facebook, LinkedIn, Snapchat, WhatsApp, Telegram).
- **Daily_Usage_Time (minutes)**: The amount of time spent on the platform per day, measured in minutes.
- **Posts_Per_Day**: The number of posts made per day.
- **Likes_Received_Per_Day**: The number of likes received per day.
- **Comments_Received_Per_Day**: The number of comments received per day.
- **Messages_Sent_Per_Day**: The number of messages sent per day.
- **Dominant_Emotion**: The user's dominant emotional state throughout the day (e.g., Happiness, Sadness, Anger, Anxiety, Boredom, Neutral).

## Data Preparation

### Data Cleaning
During data cleaning, columns with missing values were identified and filled using appropriate methods such as mean, median, or mode to ensure data integrity and quality for the model's training, testing, and validation processes.

## Exploratory Data Analysis (EDA)

### Age Distribution
- **Age Range**: The ages range from 21 to 34 years old.
- **Peak Frequency**: The most common age is 28, with a significant peak.
- **Distribution**: The distribution shows skewness towards age 28.

### Gender Distributions
- **Categories**: Female, Male, and Non-binary.
- **Frequency**: The distribution is relatively balanced between female and male, with fewer non-binary participants.

### Platform Distribution
- **Instagram** is the most used platform, followed by Twitter and Facebook.
- **WhatsApp, Telegram, and Snapchat** are the least used platforms.

### Daily Usage Time Distribution
- Most users spend between 60 and 100 minutes daily on social media, with usage tapering off after 120 minutes.

### Posts Per Day Distribution
- Most users post between 1 and 3 times per day, with a decline in the number of users posting more frequently.

### Likes Per Day Distribution
- Most users receive between 10 and 40 likes per day, with higher numbers of likes being less common.

### Comments Per Day Distribution
- Most users receive between 5 and 20 comments per day, with a peak around 5 to 10 comments.

### Messages Per Day Distribution
- Most users send between 10 and 30 messages per day, with a peak around 20 to 30 messages.

### Emotion Distribution
- **Happiness** and **Neutral** are the most prevalent emotions, while **Anger** is the least common.

### Gender and Platform Relationship
- **Instagram** and **Twitter** are the most used platforms across different genders, with variations in preferences.

### Age and Gender Relationship
- The age group around 28 years is the most diverse, with significant representation from all three gender categories.

### Platform and Emotions Relationship
- Different platforms evoke different dominant emotions, with Instagram associated with happiness and Twitter with sadness.

### Time Usage and Dominant Emotions Relationship
- **Shorter Usage Time (40-60 minutes)** is associated with negative emotions like boredom and anxiety.
- **Longer Usage Time (100-140 minutes)** is more associated with happiness.

## Modeling

### Transformer Model
The Transformer model, known for its self-attention mechanisms, is highly effective in capturing long-range dependencies in sequential data. It offers advantages in parallelization, scalability, and handling of long-term dependencies.

### BiLSTM Model
The BiLSTM model processes input sequences in both forward and backward directions, making it particularly effective in capturing contextual information in sequential data.

## Evaluation

### Transformer
- The Transformer model achieve 97% accuracy and performs well across all classes, with high precision, recall, and f1-scores. There is a slight dip in performance for anger and sadness classes.

### BiLSTM
- The BiLSTM model achive 99% accuracy and exhibits near-perfect classification performance across all emotions, with a minimal decrease in recall for anxiety and precision for sadness.

## Conclusion
The model's high accuracy and balanced performance across various emotions suggest it is well-optimized for the task. The data insights reveal that emotional experiences on social media are heavily influenced by platform choice and usage patterns, with different platforms fostering distinct emotional landscapes. These insights can be leveraged to develop targeted strategies for improving user experiences on social media, such as content moderation or platform-specific mental health interventions. Additionally, understanding how time spent on social media correlates with emotional states can help in designing tools or guidelines to promote healthier social media usage habits.
