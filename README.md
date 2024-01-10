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
