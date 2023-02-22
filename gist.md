# Understanding an email regular expression (regex)

Most of us use email or at least know what they are. Let's say I have a lengthy document and want to find all the email addresses in it. Given that email address are unique, how could we identify only the email addresses? 
This is where a regular expression, also known as regex, is extremely helpful.  A regex is a sequence of characters that specifies a search pattern in text. 
A regex can also be used to validate an input.

## Summary

In this tutorial, I will explain the regex for matching an email address.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Author](#author)

## Regex Components
An email address is comprised of some number of characters followed by an @ symbol, followed by some characters, followed by a period (.), followed by some characters. Now, let's go into detail breaking down parts of the regex matching email.
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

A forward-slash / marks the start and end of the regex. We see this as the first and last characters of the regex above.

### Anchors
^ and $ are anchors. 
^ matches the starting position, meaning the beginning of a line or string.   We see this as the second character of the email regex.
$ matches the end of a line or string. We see this as the second to last character of the email regex.

### Quantifiers
Curly brackets {} denote quantifiers.
{2,6} in this email regex means two to six characters long. 

The plus sign + indicates one or more occurances of the PRECEDING element. In the email regex, this shows up twice, once within the first set of parentheses () before the @ symbol and once within the second set of parentheses () after the @ symbol. 

### Character Classes
/d matches any digit.

### Grouping and Capturing
() denote a capturing group.
+ matches the previous item (in this case everything between the [] square brackets). 
([a-z0-9_\.-]+)  matches one or more occurrences of the characters within the bracket expressions.

### Bracket Expressions
The bracket expression [] matches any one of the characters inside these brackets.  
Let's break down the bracket expressions of this email regex.
1.  '[a-z0-9_\.-]' :  This matches the portion before the @ symbol. 'a-z' matches lower case letters of the alphabet, '0-9' matches number digits zero to nine, '_' matches underscore character, '\.' matches a period character, and '-' matches a hyphen character. 

2.  '[\da-z\.-]' : This matches the portion immediately after the @ symbol.  '\d' matches any number digit (zero to nine), 'a-z' matches lower case letters of the alphabet, '\.' matches a period character, and '-' matches a hyphen character.

3. '[a-z\.]' : This is the final bracketing expression in the email regex. 'a-z' matches lower case letters of the alphabet and '\.' matches a period character.


## Author

Anita Banh
GitHub profile: https://github.com/AnitaBanh
