# Autocorrect_NLP
Building an Autocorrect Feature using NLP with Python:

There are 4 key steps to building an autocorrect model that corrects spelling errors:

1:- Identify Misspelled Word — Let us consider an example, how would we get to know the word “drea” is spelled incorrectly or correctly? If a word is spelled correctly then the word will be found in a dictionary and if it is not there then it is probably a Misspelled Word. Hence, when a word is not found in a dictionary then we will flag it for correction.

2:- Find ‘n’ Strings Edit distance away — An edit is one of the operations which is performed on a string in order to transform it into another String, and n is nothing but the edit distance that is an edit distance like- 1, 2, 3, so on… which will count the number of edit operations that to be performed. Hence, the edit distance n tells us that how many operations are away from one string to another. Following are the different types of edits:-

Insert (will add a letter)
Delete (will remove a letter)
Switch (it will swap two nearby letters)
Replace (exchange one letter to another one)
With these four edits, we are proficient in modifying any string. So the combination of edits allows us to find a list of all possible strings that are n edits to perform.

IMPORTANT Note: For autocorrect, we take n  usually between 1 to 3 edits.

3:- Filtering of Candidates — Here we want to consider only correctly spelled real words from our generated candidate list so we can compare the words to a known dictionary (like we did in the first step) and then filter out the words in our generated candidate list that do not appear in the known “dictionary”.

4:- Calculate Probabilities of Words — We can calculate the probabilities of words and then find the most likely word from our generated candidates with our list of actual words. This requires word frequencies that we know and the total number of words in the corpus (also known as dictionary).

In our case we used the Levenshtein distance. This distance is computed by finding the number of edits which will transform one string to another. The transformations allowed are insertion — adding a new character, deletion — deleting a character and substitution — replace one character by another. By performing these three operations, the algorithm tries to modify first string to match the second one. In the end we get a edit distance.
