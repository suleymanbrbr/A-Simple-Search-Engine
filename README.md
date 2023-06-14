# A-Simple-Search-Engine
Introduction
In this project, you will write a simple program that searches for a string in another string. There are some special searching parameters and details about it will be given in later sections. First, your program will get a string until the word “end” (case-insensitive) is present and then it will ask for a search string. Your program should be able to do multiple searches until the search string “quit” (case-insensitive) is entered. The aim of this project is to practice on string member functions and loops. Of course, you will need to use the topics that we have seen before such as if-else statements and functions, as needed.
Inputs
There are two inputs respectively; Source String and Search String. Both inputs are strings. You should note that there can be spaces between the words in the Source String (hint: use a while loop to read all words using cin). However, the source string cannot contain any characters other than numbers, letters and space in the Source String, such as punctuation. On the other hand, you can assume that there is no space or tab in the search string, a single word will be entered, and you do not need to check the input for this case. Search String must end with one of ‘+’ , ‘.’ , ‘*’,’**’ characters. (See Sample Runs). Your program should get the Source String only once, but ask multiple Search Strings until “quit” (case-insensitive) is entered.
Input Checks
All inputs must be checked. In the case of an invalid input, the program should ask for an input again and again until a correct input is entered (Hint: you may use while loop here). The rules of input check are given below:
● Source String must be concatenated with the words until the word “end” (case-insensitive) is present.
● Source String must be including only letters (Both upper and lower), digits and space character. (Hint: use ASCII table)
● Search String must end with one of the ‘+’ , ‘.’ , ‘*’ characters.
● Search String cannot be empty.
Processing, Program Flow and Output
Your program should start with an introductory explanation and a prompt for the input(see sample runs). After all the inputs are entered correctly, your program should search for the string according to the rules and print out the index of the searched word.
Please note that all searches in the string are case-sensitive, which means that if the search string is "car", it will not match with "Car". However, for the ending words "end" and "quit", your program should perform a case-insensitive check. This means that if the user enters "END", "end" or “EnD” etc. to indicate the end of the string input, the program should recognize both as the end of the input. Similarly, if the user enters "QUIT", "quit" or “QuIT” etc. to indicate the end of the search queries, the program should recognize both as the end of the search process.

Search Rules
1. Search String ends with a ‘+’: The word must start with the search string.
Example:
Enter source string: Cars are fast END Enter search string: fa+
index: 9 word: fast
2. Search String ends with a ‘.’: The word ends with search string.
Example:
Enter source string: Cars are fast END Enter search string: ars.
index: 1 word: Cars
3. Search String ends with a ‘*’: The word that does not include the search string at the beginning and the end but may contain it in the middle.
Examples:
Enter source string: Cars are fast END Enter search string: as*
index: 10 word: fast
Enter source string: alan has a goal that study in alabama END Enter search string: a*
index: 6 word: has
index: 13 word: goal
index: 18 word: that
4. Search String ends with a ‘**’: Any word containing the search string regardless of location.
Example:
Enter source string: Cars are fast END Enter search string: r**
index: 2 word: Cars
index: 6 word: are
