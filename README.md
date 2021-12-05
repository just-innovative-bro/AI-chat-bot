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
```
```python
pip install keras
```
```python
pip install pickle
```
```python
pip install nltk
```
# Files
### Intents.json – The data file which has predefined patterns and responses.  
### train_chatbot.py – In this Python file, we wrote a script to build the model and train our chatbot.  
### Words.pkl – This is a pickle file in which we store the words Python object that contains a list of our vocabulary.  
### Classes.pkl – The classes pickle file contains the list of categories.  
### Chatbot_model.h5 – This is the trained model that contains information about the model and has weights of the neurons.  
### Chatgui.py – This is the Python script in which we implemented GUI for our chatbot. Users can easily interact with the bot. 

<p align="center">
<img src=https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/12/Types-of-files-1.png>
</p>

#  5 steps to create a chatbot in Python
1. Import and load the data file
2. Preprocess data
3. Create training and testing data
4. Build the model
5. Predict the response

## Import and load the data file

First, make a file name as train_chatbot.py. We import the necessary packages for our chatbot and initialize the variables we will use in our Python project.

The data file is in JSON format so we used the json package to parse the JSON file into Python.
This is how our [intents.json](https://github.com/just-innovative-bro/AI-chat-bot/blob/main/intents.json) file looks like.

## Preprocess data
When working with text data, we need to perform various preprocessing on the data before we make a machine learning or a deep learning model. Based on the requirements we need to apply various operations to preprocess the data.

Tokenizing is the most basic and first thing you can do on text data. Tokenizing is the process of breaking the whole text into small parts like words.

Here we iterate through the patterns and tokenize the sentence using nltk.word_tokenize() function and append each word in the words list. We also create a list of classes for our tags.

Now we will lemmatize each word and remove duplicate words from the list. Lemmatizing is the process of converting a word into its lemma form and then creating a pickle file to store the Python objects which we will use while predicting.

## Create training and testing data
Now, we will create the training data in which we will provide the input and the output. Our input will be the pattern and output will be the class our input pattern belongs to. But the computer doesn’t understand text so we will convert text into numbers.

## Build the model

We have our training data ready, now we will build a deep neural network that has 3 layers. We use the Keras sequential API for this. After training the model for 200 epochs, we achieved 100% accuracy on our model. Let us save the model as ‘chatbot_model.h5’.

## Predict the response (Graphical User Interface)

To predict the sentences and get a response from the user to let us create a new file ‘chatapp.py’.

We will load the trained model and then use a graphical user interface that will predict the response from the bot. The model will only tell us the class it belongs to, so we will implement some functions which will identify the class and then retrieve us a random response from the list of responses.

Again we import the necessary packages and load the ‘words.pkl’ and ‘classes.pkl’ pickle files which we have created when we trained our mode
To predict the class, we will need to provide input in the same way as we did while training. So we will create some functions that will perform text preprocessing and then predict the class.

After predicting the class, we will get a random response from the list of intents.

Now we will develop a graphical user interface. Let’s use Tkinter library which is shipped with tons of useful libraries for GUI. We will take the input message from the user and then use the helper functions we have created to get the response from the bot and display it on the GUI. Here is the full source code for the GUI.

## Run the chatbot
To run the chatbot, we have two main files; train_chatbot.py and chatapp.py.

First, we train the model using the command in the terminal:
```python
python train_chatbot.py
```
<p align="center">
<img src=https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/12/chatbot-result.png>
 </p> 

If we don’t see any error during training, we have successfully created the model. Then to run the app, we run the second file:
```python
python chatgui.py
```
<p align="center">
<img src=https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/12/chat-between-user-bot.png>
</p>
