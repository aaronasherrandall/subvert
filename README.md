# subvert
Program for checking Terms &amp; Conditions to see if company plans on selling your data.

50 documents that we know sell data:

- Terms & Conditions
- Contracts
- Terms of Use
- Privacy Policy

1. Use python script to eliminate erroneous English words:
https://www.geeksforgeeks.org/removing-stop-words-nltk-python/

Example using stopwords

1. Have .py and .txt in same directory
2. .py outputs new .txt file without stopwords

```Python
import io 
import nltk
nltk.download('stopwords')
from nltk.corpus import stopwords 
from nltk.tokenize import word_tokenize 
# word_tokenize accepts a string as an input, not a file. 
stop_words = set(stopwords.words('english')) 
file1 = open("text.txt") 
line = file1.read()# Use this to read file content as a stream: 
words = line.split() 
for r in words: 
    if not r in stop_words: 
        appendFile = open('filteredtext.txt','a') 
        appendFile.write(" "+r) 
        appendFile.close()
```

