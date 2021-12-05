# AI-chat-bot
A chatbot is an intelligent piece of software that is capable of communicating and performing actions similar to a human. Chatbots are used a lot in customer interaction, marketing on social network sites and instantly messaging the client. There are two basic types of chatbot models based on how they are built; Retrieval based and Generative based models.

# Generative based Chatbots
Generative models are not based on some predefined responses.

They are based on seq 2 seq neural networks. It is the same idea as machine translation. In machine translation, we translate the source code from one language to another language but here, we are going to transform input into an output. It needs a large amount of data and it is based on Deep Neural networks.

# Execution
<img src=https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/12/Python-chatbot-project.gif>

# Prerequisites
```python
pip install tensorflow
pip install keras
pip install pickle
pip install nltk
```
# Files
Intents.json – The data file which has predefined patterns and responses.  
train_chatbot.py – In this Python file, we wrote a script to build the model and train our chatbot.  
Words.pkl – This is a pickle file in which we store the words Python object that contains a list of our vocabulary.  
Classes.pkl – The classes pickle file contains the list of categories.  
Chatbot_model.h5 – This is the trained model that contains information about the model and has weights of the neurons.  
Chatgui.py – This is the Python script in which we implemented GUI for our chatbot. Users can easily interact with the bot. 

#  5 steps to create a chatbot in Python
1. Import and load the data file
2. Preprocess data
3. Create training and testing data
4. Build the model
5. Predict the response

## Import and load the data file

First, make a file name as train_chatbot.py. We import the necessary packages for our chatbot and initialize the variables we will use in our Python project.

The data file is in JSON format so we used the json package to parse the JSON file into Python.
This is how our intents.json file looks like.
