# week 3

## Text wrangling

### CSVs

"Comma separated values"

### Analog coding

Interpreting a text according to a theme

Qualitative process

#### Group activity: analog coding
read excerpt and identify works/phrases relating to gendered work.

##### phrases:

- secretary x3
- married x3
- traditional x1
- retire x1
- babies x1
- husband x2
- family x3
- our level x1
- capable x1
- raising x1
- professional x1
- doing this x1
- do something else x1
- career x1

### Programming

Like writing an essay.

Code should be clear and concise and well-document/annotated.

#### Python

"High level" language: closer to the language you naturally speak (vs the language your computer speaks).

"Low level" includes languages like C.

Easier to "debug" the code thanks to clear error messages.

Processes data relatively quickly.

Automates some functions which can impact efficiency/speed. Will be seen when analyzing very large data sets. Cost of being programmer friendly vs machine friendly.

#### Jupyter Notebook

Environment in which we will write Python.

Can run individual chunks of code.

Keeps projects in steps of coding in one place rather than in individual files.

Allows commentary to be added to code via Markdwn which helps your work be reproducible. Other people will be able to confirm your results. Increases transparency. Many publications are now asking for DH projects to include the code.

#### Why not use Voyant/etc?

Transparency: you don't see the code, only the results. Writing the code yourself allows you to see how conclusions are come to.

### git clone

```git clone [repository https link]```

clone a given repository.


### Python analysis intro

```
# importing regex library that allows you to search for specific chunks in a string/separate a string based on a character
import re
# importing the collections library, but only the counter function
from collections import Counter

# a string
# defining a variable that stores name of file to open in a string
filepath_of_text = "Bette-Smith-Transcript.txt"

# an integer
# number of words to look at when tallied; i.e., top 50
number_of_desired_words = 50

# a list
# an array listing words to ignore
stopwords = ['i', 'me', 'my', 'myself', 'we', 'our', 'ours', 'ourselves', 'you', "you're", "you've", "you'll", 
             "you'd", 'your', 'yours', 'yourself', 'yourselves', 'he', 'him', 'his', 'himself', 'she', "she's", 
             'her', 'hers', 'herself', 'it', "it's", 'its', 'itself', 'they', 'them', 'their', 'theirs', 
             'themselves', 'what', 'which', 'who', 'whom', 'this', 'that', "that'll", 'these', 'those', 'am', 'is', 
             'are', 'was', 'were', 'be', 'been', 'being', 'have', 'has', 'had', 'having', 'do', 'does', 'did', 'said', 
             'say', 'doing', 'a', 'an', 'the', 'and', 'but', 'if', 'or', 'because', 'as', 'until', 'while', 'of', 'at',
             'by', 'for', 'with', 'about', 'against', 'between', 'into', 'through', 'during', 'before', 'after', 
             'above', 'below', 'to', 'from', 'up', 'down', 'in', 'out', 'on', 'off', 'over', 'under', 'again', 
             'further', 'then', 'once', 'here', 'there', 'when', 'where', 'why', 'how', 'would', 'could', 'should', 
             'all', 'any', 'both', 'each', 'few', 'more', 'most', 'other', 'some', 'such', 'no', 'nor', 'not', 'only', 
             'own', 'same', 'so', 'than', 'too', 'very', 's', 't', 'can', 'will', 'just', 'don', "don't", 'should', 
             "should've", 'now', 'd', 'll', 'm', 'o', 're', 've', 'y', 'ain', 'aren', "aren't", 'couldn', "couldn't", 
             'didn', "didn't", 'doesn', "doesn't", 'hadn', "hadn't", 'hasn', "hasn't", 'haven', "haven't", 'isn', 
             "isn't", 'ma', 'mightn', "mightn't", 'mustn', "mustn't", 'needn', "needn't", 'shan', "shan't", 'shouldn', 
             "shouldn't", 'wasn', "wasn't", 'weren', "weren't", 'won', "won't", 'wouldn', "wouldn't"]

# body paragraphs

# file io
# defining and storing value of the entire text in a variable; opens the file stored in the variable above, make it all lowercase
full_text = open(filepath_of_text, encoding="utf-8").read().lower()

# words of text split using regex --> text transforms from string to list
# analyzes the text to turns/splits it into an array of individual words
text_split_into_words = re.split(r"\W+", full_text)

# empty list
# loop to remove stopwords and populate significant_words with... the significant words
# defines an empty array that the for loop then populates with words from the text-turned-list, given that it doesn't appear in the stopwords array and is alphabetical (not a number)
significant_words = []

for word in text_split_into_words:
    if word not in stopwords and word.isalpha():
        significant_words.append(word)

# a dictionary
# counting the words that occur in the significant_words array and defining the most common
significant_words_tally = Counter(significant_words)
order_significant_words = significant_words_tally.most_common(number_of_desired_words)

order_significant_words
```

