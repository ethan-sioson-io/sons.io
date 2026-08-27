# ECE 2112 Programming Assessment 1
**Ethan Joseph L. Sioson** | **2ECE-C**<br>
_This repository contains three programming problems which covers **Module 1 - Base Computing with Python.**_<br>
**Objectives:**<br>

1. use basic Python functions, operators, and string operations;
2. manipulate strings using indexing, slicing, and built-in string methods;
3. apply sequence unpacking to manipulate the elements of a list; and
4. construct simple Python functions that return a specified result.

## A. Word Rotation Problem
Create a function named `rotate word()` that accepts a non-empty string. Move the **first character**
of the string to the end while keeping all remaining characters in their original order. Preserve the
capitalization of every character.

### Code for the Problem:
```ruby
def rotate_word(text):
    return text[1:] + text[0]
```
- `text[1:]`: This utilizes **string slicing** to take the character starting from the **second index** to the end of the text.
- `text[0]`: This utilizes **string indexing** to take the character from the **first index** only.

## B. Username Builder Problem
Create a function named `make username()` that accepts two strings: **first name** and **last name**. The
function must:<br>
1. convert all letters to lowercase;
2. remove all spaces from the first name;
3. remove all spaces from the last name; and
4. join the processed first and last names using one period (.).

### Code for the Problem:
```ruby
def create_username(firstname, lastname):
  username = firstname+"."+lastname
  username = username.lower()
  username = username.replace(" ","")
  return username
```
- `firstname+"."+lastname`: This joins the input from the firstname, the period character, and lastname together.
- `username.lower()`: This converts every uppercase letter to lowercase.
- `username.replace(" ","")`: This replaces any spaces in the string with an empty string to delete them.

## C. Bookend Swap Problem
Create a function named `swap bookends()` that accepts a list containing **at least** two elements. Unpack
the list into three variables:<br>
• **first** – the first element;
• **middle** – a list containing everything between the first and last elements; and
• **last** – the last element.
Using these variables, return a **new list** in which the first and last elements have exchanged positions.
The elements in **middle** must remain in their original order. Do not modify the input list.

### Code for the Problem:
```ruby
def swap_bookends(items):
  first = items[0]
  last = items[-1]
  middle = items[1:-1]
  items = last, *middle, first
  return items
```
- `first = items[0]`: This takes the first item in the list at index 0.
- `last = items[-1]`: This takes the last item in the list at index -1.
- `middle = items[1:-1]`: This utilizes string slicing to take the items from index 1 until, but not counting, index -1 (takes the values between the first and last items).
- `items = last, *middle, first`: This converts every uppercase letter to lowercase.

## Edit History:
August 27, 2026 - Added descriptions, codes, and explanations for PA1 (A, B, and C).
