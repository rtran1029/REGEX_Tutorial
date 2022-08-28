# REGEX_Tutorial

A basic tutorial on Regular Expressions.

## Summary

In short, Regex stands for regular expressions. Regex utilizes characters to define specific search patterns. For example, the following regex defines a search for and email address.

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
-----
### **Anchors**  `^` and `$`

These characters start and end a string respectively.  They indicate that whatever is between them is what will need to be matched in order to complete the search.  

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

-----

### **Quantifiers** `+` and `{x, y}`
`+`

This "`+`" will perform a match of characters defined to the left of the quantifier.

([a-z0-9_\.-]`+`)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Here it matches any combination of lowercase characters, numbers, periods, underscores or dashes.  

`{x, y}`

In our example, these quantifiers indicate that we want to find an expression between 2 and 6 in length.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]`{2,6}`)$/

-----

### **OR Operator** `(|or|)`

Alternation is the term in regular expression that is actually a simple “OR”. It is denoted as this vertical character `|`

our example does not have any OR alternation operators but here is an example i found online.

For example, the following expression will match either 'abc' or '123':

/abc`|`123/

-----

### **Character Classes** `\.` and `\d`
`\.`

These will match any periods given in an expression:

/^([a-z0-9_`\.`-]+)@([\da-z`\.`-]+)\.([a-z`\.`]`{2,6})$/

`\d`
These will match any single characters that are digits from 0-9:

/^([a-z0-9_\.-]+)@([`\d`a-z\.-]+)\.([a-z\.]{2,6})$/

-----

### **Flags** `//`

Flags are the forward slashes // that begin and end the regex:

`/`^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$`/`

-----

### **Grouping and Capturing** `()`

Parentheses `()` are used in regular expressions to group together different parts of the search. In our Regex expression there are 3 grouped sections:

/^`(`[a-z0-9_.-]+`)`@`(`[\da-z.-]+`)`.`(`[a-z.]{2,6}`)`$/

`([a-z0-9_.-]+)` - characters before the @ sign in an email address<br>
`([\da-z.-]+)` - characters after the @ sign in an email address<br>
`([a-z.]{2,6})` - the domain after the dot . at the end of the email address<br>

-----

### **Bracket Expressions** `[]`

These will include everything within the OR Operator brackets as a parameter for the match/search. In our example these are included within the OR Operators.

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

`[a-z0-9_\.-]` - Matches any lowercase letters, numbers 0-9, underscores, periods or dashes<br>
`[\da-z\.-]` - Matches any single digit, lowercase letters, periods or dashes<br>
`[a-z\.]` - matches any lowercase letters and periods<br>


-----

### **Greedy and Lazy Match** `+` vs `+?`

With my limited understanding of it, what i can draw is that a greedy match will search every character withing the defined expression indiscriminantly and as many times as necessary until completed. Where as a lazy match will repeat the match a minimal amount of times to satisfy the search parameter.

-----

### **Boundaries**

Boundaries work by matching strings and their positioning within words and phrases. For instance, "`\b`" matches a word boundary between a word character and a non-word. the position of the word is also important to the the results of the word search here is a quick example below

`\b`dog`\b` - would match *dog* in "hairy *dog*" but not in "hot*dog*" or "*dog*gy"<br>
`\b`dog - would match *dog* in "*dog*gy" and in in "hairy *dog*" but not in "hot*dog*"<br>
dog`\b` - would match *dog* in "hot*dog*" and in "hairy *dog*" but not in "*dog*gy"<br>

-----

### **Back-references** `\{number}` or `\{word}` 

Back-references allow the user to repeat a capturing group. It's used inside a regex by inlining its group number preceded by a single backslash. within our example

/^([a-z0-9_\.-]+)@`([\da-z\.-]+)`\.([a-z\.]{2,6})$/

if i wanted to reference just the second capturing group i would utilize `\2`<br>
this would reference this group from the example above `([\da-z\.-]+)`<br>

-----

### **Look-ahead and Look-behind**

Look-ahead and look-behind matches fall under the "look-around" patterns. Look-around lets you match a group before (look-behind) or after (look-ahead) your main pattern without including it in the result.

-----

-----




## **Author**

Richard Tran made this tutorial as a part of completion requirements for the GT-Bootcamp. Thank you for your time and I hope some of this can be helpful to your development endeavors.

https://github.com/rtran1029/REGEX_Tutorial

https://gist.github.com/rtran1029/bbbf2f4f7d6dcfc663d7719d9ee4d280

-----
