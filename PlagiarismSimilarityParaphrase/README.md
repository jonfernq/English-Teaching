## Plagiarism, Similarity, & Paraphrase 

Below is some code to check whether a ChatGPT paraphrase of text in a communicative language learning textbook is sufficiently different 
to not be categorized as plagiarism. The code uses the [Jaccard similarity coefficient](https://en.wikipedia.org/wiki/Jaccard_index#:~:text=The%20Jaccard%20coefficient%20is%20widely,to%20bags%2C%20i.e.%2C%20Multisets.): 

```python
from sklearn.feature_extraction.text import CountVectorizer

# Define the two paragraphs to compare
paragraph1 = "Information gap activities are a common approach to English language learning that involves providing students with tasks or challenges that require them to acquire new information in order to be successful. These activities typically involve a scenario in which one student (Student A) possesses information that the other student (Student B) does not, and Student B must gather that information in order to complete the task or solve the problem. Information gap activities may be one-sided or reciprocal, and can be played in pairs or small groups, with each member of the group possessing some unique piece of information."

paragraph2 = "The simplest activities are based on the information gap principle. In these activities Student A has access to some information which is not held by Student B. Student B must acquire this information to complete a task successfully. This type of game may be one-sided, as in the above example, or reciprocal, where both players have information which they must pool to solve a common problem. The games may be played in pairs or in small groups, where all the members of the group have some information."

# Define the Jaccard similarity threshold
threshold = 0.6

# Convert the paragraphs to sets of words
set1 = set(paragraph1.split())
set2 = set(paragraph2.split())

# Calculate the Jaccard similarity coefficient
jaccard_similarity = len(set1.intersection(set2)) / len(set1.union(set2))

# Compare the Jaccard similarity coefficient against the threshold
if jaccard_similarity >= threshold:
    print("Potential plagiarism detected.")
else:
    print("No potential plagiarism detected.")
```
