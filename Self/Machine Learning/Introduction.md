#machine-learning


## What is machine learning? 

Machine learning is an ability for a computer to learn how to solve problems without explicit direction. 

## Why use machine learning? 
Machine learning is best for cases where it is difficult to provide explicit step by step direction to solve a problem. 
For example voice and image recognition are good examples. Since there is no explicit step by step instruction to identify if there is a face in a given picture, machine learning is a good use case. 
## Types of machine learning systems. 

Types of machine learning is divided by three big categories

> [!NOTE] Features, targets
> Features - x axis
> Targets - y axis 

### Training Supervision
A model's training supervision can either be supervised, unsupervised, semi-supervised, self-supervised or reinforcement. 
### Supervised
In supervised learning, the training set you feed to the algorithm includes the desired solution. 
* For example, the training data to train an algorithm to detect if an email is spam or not contains a row that indicates whether the email is an spam. 

The typical tasks for supervised learning includes **classification** and **regression**

**Classification** - yes/no. The spam filter is an example. 

**Regression** - Predicting the price of a car given it's features and conditions. Or a home price given the home's features (area, bedrooms, bathrooms, neighborhood, etc.)
### Unsupervised
Unlike supervised training, the trading data is unlabeled. 
- Example: Running a clustering algorithm to attempt to detect groups of similar visitors to a website for a targeted communication. 

The common use cases for unsupervised algorithms include: 
1. Dimensionality reduction / feature extraction
	1. Process of simplifying the data without losing too much information. 
	2. Merging several correlating features into a single feature. 
		1. Example: Milage and the age of a car when predicting a car price. 
2. Anomaly detection
	1. Examples include: 
		1. Detecting unusual credit card transactions to prevent fraud. 
		2. Catching manufacturing defects. 
	2. Can also be used to clean up training data before feeding the data to another training model.
3. Association rule learning - looking at a dataset and discovering relations between them. 
	1. Example: In a grocery store, people who buy marshmallow, chocolate and graham crackers also tend to buy firewood. So the store might consider placing firewood by the other three. 
#### Semi-Supervised
A combination of supervised and unsupervised learning. 
- Example: Google photos, face detection. 
	- Google's algorithm automatically detects and identifies uniques faces. (unsupervised)
	- The google photos user has to confirm the edge cases and provide names to those faces (supervised)
#### Self-Supervised
Model that learns from unlabeled data by creating its own supervisory signal from the data itself, rather than relying on explicit human-provided labels. This approach falls between supervised learning (which requires labeled data) and unsupervised learning.
- In computer vision: Predicting missing parts of images, colorizing grayscale images, or predicting the relative position of image patches
- In NLP: Predicting masked words in sentences (like BERT), or predicting the next word in a sequence (like GPT models)
- In sequence modeling: Predicting future frames in videos or future states in time series data
#### Reinforcement
This learning model has an **agent** that can observe the environment and perform actions. In return the agent gets rewards (for positive actions) and penalties for negative actions (in form of negative rewards). 
- The agent must learn by itself what the best course of action is, called **policies** and aims to get the most rewards. 
- Examples include: 
	- robots that do physical tasks like walk, or move items. 
	- chess/go bots. 
### Batch vs Online Learning
#### Batch Learning
The AI Model is trained using all available data. Once the system is trained, it is launched into production and runs without further training. 
- Periodic training needed in order to update the model to handle new scenario
- Example: for a spam filter, train it to include new spam filters. 
#### Online Learning
Training the model incrementally by feeding it data instances sequentially called *mini batches*. 
* The system can learn about new data on the fly. 
* Example: For spam filter, automatically recognize and update model. ww
