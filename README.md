# REGEX_Tutorial

A basic tutorial on Regular Expressions.

## Summary

In short, Regex stands for regular expressions. Regex utializes characters to define specific search patterns. For example, the following regex defines a search for and email address.

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
-----

### **Anchors**  
`^` and `$`

These characters start and end a string respectively.  They indicate that whatever is between them is what will need to be matched in order to complete the search.  

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

-----

### **Quantifiers**
`+`

This "`+`" will perform a match of characters defined to the left of the quantifier.

([a-z0-9_\.-]`+`)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Here it matches any combination of lowercase characters, numbers, periods, underscores or dashes.  

`{x, y}`

In our example, these quantifiers indicate that we want to find an expression between 2 and 6 in length.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]`{2,6}`)$/

-----

### **OR Operator**
`[]`

These will include everything within the OR Operator brackets as a paramiter for the match/search. In our example these are included within the OR Operators.

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

`[a-z0-9_\.-]` - Matches any lowercase letters, numbers 0-9, underscores, periods or dashes<br>
`[\da-z\.-]` - Matches any single digit, lowercase letters, periods or dashes<br>
`[a-z\.]` - matches any lowercase letters and periods<br>

-----

### **Character Classes**

-----

### **Flags**

-----

### **Grouping and Capturing**

-----

### **Bracket Expressions**

-----

### **Greedy and Lazy Match**

-----

### **Boundaries**

-----

### **Back-references**

-----

### **Look-ahead and Look-behind**

-----

## **Author**

-----
A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
