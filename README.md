# NLP_notes

## Regular Expression
1. Positive Lookahead
For example, consider the regex X(?=Y). This will match 'X' only if 'X' is immediately followed by 'Y'. However, it will not include 'Y' in the match result.
Here's a practical example:
```
Suppose you have the string "John123Doe456".
You want to find all the numbers that are immediately followed by a letter but don't want the letters themselves in the match.
Using a positive lookahead, the regex could be \d+(?=[A-Za-z]).
This regex will match '123' and '456', as they are followed by 'D' and 'o' respectively, but 'D' and 'o' will not be part of the matched results.
```

## How to analyze a column in a dataframe?
```
df["comments_tokenized"] = df["comments"].map(lambda x: [nltk.tokenize.word_tokenize(i) for i in x])
```
1. Map is a method in pandas that applies a given function to each item in a Series (here, the "comments" column in the DataFrame).
2. Lambda Function:
   lambda x: ... is an anonymous function in Python. Here, x represents each element in the "comments" column. Inside the lambda function, there's a list comprehension: [nltk.tokenize.word_tokenize(i) for i in x].
This list comprehension iterates over x. Here, x is expected to be an iterable (like a string or a list of strings). Each element in this iterable is represented by i. For each i, the function nltk.tokenize.word_tokenize(i) is called.
