# Anagram_Finder
**Introduction:**

Welcome to the Anagram Finder! This Python script helps you find anagrams in a list of words. Anagrams are words or phrases formed by rearranging the letters of another word or phrase, using all the original letters exactly once.

**How it Works:**

is_anagram(word1, word2)
This function takes two words, word1 and word2, as input parameters and checks if they are anagrams of each other.
1. The function first converts both words to lowercase to make the comparison case-insensitive.
2. Then, it sorts the characters of each word alphabetically using the sorted() function.
3. Finally, it compares the sorted versions of the two words using the equality (==) operator and returns the result.
   
find_anagrams(words)
The find_anagrams function takes a list of words, words, as input and finds anagram groups within the list.
1. It initializes two empty lists, anagrams and non_anagrams, to store the found anagrams and words without any anagrams, respectively.
2. It creates a set called recorded to keep track of words that have already been processed, avoiding duplicate processing.
   
Main Loop
1. The function iterates through the list of words one by one.
2. For each word, it checks if it has not been processed before (i.e., not present in the recorded set).
   
Finding Anagrams
1. For each unprocessed word, it creates a new list called current_anagram to store the current anagram group starting with the current word.
2. It then loops through the rest of the words to find anagrams of the current word.
3. If a word is an anagram of the current word (using is_anagram), it is added to the current_anagram list, and it's marked as recorded.
4. This process continues until all words are checked for anagrams against the current word.
   
Grouping Anagrams
1. If there are more than one words in the current_anagram list, it means that the current word has anagrams in the given list.
2. The current_anagram list is then appended to the anagrams list, forming an anagram group.

Handling Non-Anagrams
1. If the current_anagram list has only one word, it means that the word doesn't have any anagrams in the list.
2. In this case, the word is appended to the non_anagrams list.

**Running the Script:**

1. The main section of the code prompts the user to enter a list of words separated by spaces.
2. The user's input is split into individual words and stored in the word_list variable.
3. The find_anagrams function is called with word_list as the input.
3. The function returns two lists: anagrams containing the anagram groups and non_anagrams containing words without anagrams.
4. The results are then printed to the console.

**Opening the Code in Google Colab:**

1. To open and run the code in Google Colab, follow these steps:
2. Go to the GitHub repository containing the code.
3. Click on the .ipynb notebook file.
4. On the top-right corner of the notebook page, you'll see a "Open in Colab" button. Click on it to open the notebook in Google Colab.
5. Google Colab will open the notebook in a new tab. You can now run the code.
