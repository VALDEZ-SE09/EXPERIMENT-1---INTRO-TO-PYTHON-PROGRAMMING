# Experiment - 1 : INTRODUCTION TO PYTHON PROGRAMMING

## Objective:

> To identify the basic codes and functions in Python Programming

> To be able to apply the different codes and functions in creating a Python program

## Problem 1: Alphabet Soup Problem

### Expected Behavior: 

> Create a function that takes a string and returns a string with its letters in alphabetical order.

### Approach:

> Define a function that accepts a string as input.

> Use Python’s built-in sorted() function to sort the letters.

> Join the sorted letters back into a string and return it.

### Start of Code:

#sort letters of string into alphabetical order

def sortString(s):
    return ''.join(sorted(s)) #join sorted characters into a string

s = 'Advanced Programming and Algorithms'

print(sortString(s))  

>> Output: AAPaaacdddeggghiilmmmnnnoorrrstv

s = 'Electronics and Communications Engineering'

print(sortString(s))

>> Output: CEEaacccdeeeggiiiiilmmnnnnnnnooorrssttu

s = 'My Dearest Ashley'

print(sortString(s))

>> Output: ADMaeeehlrsstyy

## Problem 2: Emoticon Problem

### Expected Behavior:

> Create a function that changes specific words into emoticons.
> Replace the words smile, grin, sad, and mad with their corresponding emoticons:

smile → :)

grin → :D

sad → :(

mad → >:(

### Approach:

> Define a dictionary to map specific words to emoticons.

> Split the sentence into words and replace matches with their corresponding emoticon.

> Return the updated sentence.

### Start of Code:

#replacing words with emoticons

def emoticons(sentence):
    emoticon_dict = {
        "smile" : ":)",
        "grin" : ":D",
        "sad" : ":((",
        "mad" : ">:("
    }
    
#split sentence into words
 
  words = sentence.split()
    
#replace words with corresponding emoticons
  
  replaced_emoticons = " ".join([emoticon_dict.get(word, word) for word in words])
 
  return replaced_emoticons

  sentence = "You make me smile"
  
  result = emoticons(sentence)
  
  print(result)   
  
  >> Output:  You make me :)

  sentence = "She has beautiful eyes and a wide grin"
 
  result = emoticons(sentence)
  
  print(result)   
  
  >> Output: She has beautiful eyes and a wide :D

  sentence = "I am sad because I had to retake this course"
 
  result = emoticons(sentence)
  
  print(result)   
  
  >> Output: I am :(( because I had to retake this course

  sentence = "I get mad when people walk slowly"
  
  result = emoticons(sentence)
  
  print(result)   
  
  >> Output: I get >:( when people walk slowly


## Problem 3: Unpacking List Problem

###  Expected Behavior:

> Unpack a given list into three variables:
  >> first → first element
  >> middle → all elements between the first and last
  >> last → last element

### Approach:

> Use list slicing to assign the first, middle, and last values to separate variables.

> Print all three variables.

### Start of Code:
#example list of numbers
my_list = [1,8,4,8,6,2]

#unpacking the list
first, *middle, last = my_list
print(f"first: {first}, middle: {middle}, last: {last}")

>> Output: first: 1, middle: [8, 4, 8, 6], last: 2

#example list of numbers
my_list = [1,1,0,9,2,3]

#unpacking the list
first, *middle, last = my_list
print(f"first: {first}, middle: {middle}, last: {last}")

>> Output: first: 1, middle: [1, 0, 9, 2], last: 3

#example list of programming languages
my_list = ['C++', 'Python', 'Java', 'Visual Basic']

#unpacking the list
first, *middle, last = my_list
print(f"first: {first}, middle: {middle}, last: {last}")

>> Output: first: C++, middle: ['Python', 'Java'], last: Visual Basic

