# Understanding an email regular expression (regex)

Most of us use email or at least know what they are. Let's say I have a lengthy document and want to find all the email addresses in it. Given that email address are unique, how could we identify only the email addresses? 
This is where a regular expression, also known as regex, is extremely helpful.  A regex is a sequence of characters that specifies a search pattern in text. 
A regex can also be used to validate an input.

GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile

## Summary

In this tutorial, I will explain the regex for matching an email address.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
An email address is comprised of some number of characters followed by an @ symbol, followed by some characters, followed by a period (.), followed by some characters. Now, let's go into detail breaking down parts of the regex matching email.
The forward-slash / marks the start and end of the regex.


### Anchors
^ and $ are anchors. 
^ matches the starting position, meaning the beginning of a line or string. 
$ matches the end of a line or string.

### Quantifiers

{2,6} means 2 to 6 characters long.

The plus sign + indicates one or more occurances of the PRECEDING element. In the email regex, this shows up twice, once before the @ and once after. 

### OR Operator

The OR operator, represented by "|", is not part of the email regex.

### Character Classes
/d matches any digit.
### Flags

### Grouping and Capturing

### Bracket Expressions
The bracket expression [] matches any one of the characters inside these brackets.  'a-z' matches letters a to z , '0-9' matches numbers zero to nine, '_' matches underscore, '\.' matches a period, and '-' matches a hyphen. 

+ matches the previous item (in this case everything between the [] square brackets). 



/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Greedy and Lazy Match
none
### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Anita Banh
GitHub profile: https://github.com/AnitaBanh
