# Arthrex_Assignment
Approach to Solve the "auto_suggest" problem:
First we create an empty list (matching_words) which can store the words which matches our input pattern,then we check for the input if it contains non-alphanumeric symbols.
Then we remove duplicates from the input, whether it contain multiple symbols or alphabet.
After that we have write our logic for comparing the input with the words present in the list.
Then we return the matching_words list (which contain the suggestions regarding the input).

Steps to Solve the "auto_suggest" Problem:

1.Initialization: Create an empty list matching_words to store results.
                  Initialize pattern as an empty string.

2.Handle Empty Input: If input is empty, return all words.

3.Check First Character: If the first character is a non-alphanumeric symbol:
                         Extract unique characters from inp into pattern, skipping the first symbol.
                         If no characters remain, return an empty list.

4.Set Pattern: If the first character is alphanumeric, use the entire inp as pattern.

5.Match Words: Loop through each word in words.
               Add words to matching_words if they end with or contain pattern.

6.Return Results: Return the matching_words list.

For Example: 
words = ["cake", "snake", "lake", "ack", "jazz", "zebra", "zoo", "sam"]
inp1 = "ke" 
output: ["cake", "snake", "lake"] 
exp:The function will match words that end with or contain "ke".

#Test Cases

(Case1):
inp2 = "********************************************z"
output: ['jazz', 'zebra', 'zoo']
The pattern is "z" after removing the leading symbols. The function will match words that contain "z".

(Case2):
inp3 = "*k*"
output: ['cake', 'snake', 'lake', 'ack']

(Case3):
inp4 = "!ack"
output: ['ack']
inp5 = "$"
output: []

