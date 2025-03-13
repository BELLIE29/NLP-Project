# Unit 6 - Natural Language Processing Project

## Introduction

Natural language processing (NLP) is used in many apps and devices to interact with users and make meaning of text to determine how to respond, find information, or to create new text. Your goal is to use natural language processing techniques to identify structure, patterns, and meaning in a text to have conversations with a user, execute commands, perform manipulations on the text, or generate new text.

## Requirements

Use your knowledge of object-oriented programming, ArrayLists, the String class, and algorithms to create a program that uses natural language processing techniques:

- **Create at least two ArrayLists** – Create at least two ArrayLists to store the data used in your program, such as data from text files or entered by the user.
- **Implement one or more algorithms** – Implement one or more algorithms that use loops and conditionals to find or manipulate elements in an ArrayList or String object.
- **Use methods in the String classs** - Use one or more methods in the String class in your program, such as to divide text into sentences or phrases.
- **Use at least one natural language processing technique** – Use a natural language processing technique to process, analyze, and/or generate text.
- **Document your code** – Use comments to explain the purpose of the methods and code segments and note any preconditions and postconditions.

## UML Diagram

![alt text](UMLDiagram.jpg)

## Video
Link to Youtube Video:
https://youtu.be/iJlWK9rM5mI

Thumbnail:
![alt text](NLPThumbnail.png)

## Project Description

If there is a situation where you really want to tell your friend who only speaks Spanish the name of a song you love, use our Song Title Translator! Song Title Translator gets the user input (title of any song in English) and translates it into Spanish and returns it. For example, if the user input was "love", our app analyzes that input, searches through the Original list, and finds the word in the translation word list at the same index, and returns it, so "love" would return as "amor". 
## NLP Techniques

We implemented machine translation as our natural language processing technique in our project. Our project takes user input, or a song title in English, splits it into words, checks each word individually (with wordsList) to see if there is a translation for it (translationList) at the same index, and replaces it with the translation if there is one. 

The first method that is associated with this NLP technique is our checkWords method because it is the root of our code's whole process. It checks each word the user inputted against our wordsList and returns the translated word at the same index from translatedWordList (if there is a translation, however if there is not the original word remains the same). This is necessary in the NLP technique because it makes sure that the words that are inputted correspond to the correct translation at the same index.

The next method that is associated with this NLP technique is our createWordList method, which splits the input into individual words. It does this by taking the user input as a String and uses split to break the string up into single words. Then the words are stored in the string arraylist and returns it. This method is necessary for the translation NLP because since translation NLP is word for word, the user's input must be split up or broken down into an individual list of words before being checked and translated at the same index.

Another method that is associated with translation NLP is the prompt method which is the method that interacts with each user, takes their input, and starts up the actual translation process for our code. The prompt method works when a user enters in their song title in English. It then calls the createWordList so it can split the input into words, then calls the checkWords method to do the actual translation, and then forwards the original and translated lists to the printSummary method for the output. This method is necessary for translation NLP because it starts the translation process by making sure the user input is correctly collected and processed through the other NLP steps. Without our prompt method, the program would not be able to function correctly. 

A method associated with translation NLP in our code is also the printSummary method which outputs the original and translated song titles to the user playing. It works by first printing the original list of words, then the translated list of words, and then calls the noTranslation method to see if any of the words inputted were not translated. This method is necessary for translation NLP because our user needs to see the translated version of their song, and this method presents that. This method makes sure that the user's output is clear to the user. 

The last method in our code that is associated to translation NLP is the noTranslation method, which is the method that checks to see if any of the words that were inputted were not able to be translated, and also informs the user if that is the case. It works by iterating through the Original list (wordsList) and checks the index of each word in the translatedWordList. If the word from the original list is equal to the word in the translatedWordList at the same index, then no translation happened and the message telling the user that no translation is available is printed. However if it is equal, than a translation is available and that message is not printed. This method is necessary for this NLP technique because when a word isn't able to be translated in our code we need to inform our user so. This in a way provides feedback to our user and makes our program more user-friendly. 