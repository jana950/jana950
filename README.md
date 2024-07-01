- 👋 Hi, I’m @jana950
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
jana950/jana950 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import nltk
from nltk.stem import WordNetLemmatizer

lemmatizer = WordNetLemmatizer()

# Define rules and responses
rules = [
    {'rule': 'hello', 'response': 'Hello! How can I help you?'},
    {'rule': 'thank you', 'response': 'You\'re welcome!'},
    {'rule': 'how are you', 'response': 'I\'m doing well, thanks!'},
    # Add more rules here
]

# Define a function to process user input
def process_input(input_text):
    input_text = input_text.lower()
    input_words = nltk.word_tokenize(input_text)
    input_lemmas = [lemmatizer.lemmatize(word) for word in input_words]
    input_string = ' '.join(input_lemmas)

    # Check rules and respond
    for rule in rules:
        if rule['rule'] in input_string:
            return rule['response']

    # Default response if no rule matches
    return 'Sorry, I didn\'t understand that.'

# Test the chatbot
while True:
    user_input = input('User: ')
    print('Chatbot:', process_input(user_input))


Remember to install the NLTK library and download the WordNet corpus before running this code. You can do this by running `nltk.download('wordnet')` in your Python environment.

This is a basic example, and you can improve it by adding more rules, using more advanced NLP techniques, and integrating it with a user interface or other applications.
