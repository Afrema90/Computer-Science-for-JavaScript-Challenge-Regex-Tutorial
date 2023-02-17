# Title: Regex Tutorial for Matching a URL 
This tutorial is specific to utilizing Regular Expressions (Regex) for matching URL. 


## Summary
I will be describing the expression for matching a URL for the following: /^(https?:\/\/)? ([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
During this tutorial, I will go through the expressions and break down with detailed explanation of each piece.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

Regex Components
There are a lot of components that go into building a regular expression and because regex is considered plain as simple, we should also remember that these expressions must include slash characters /. When looking at our example expression for matching a URL, we can see / at the beginning and end.

/^(https?:\/\/)? ([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

We will now be looking at each of the components that make up the above expression.

### Anchors
The anchors will be described by two characters seen throughout regular expressions. we will be looking at ^ and the $ -- which signifying what we will be looking for at the beginning and end of the string. when you look at it, it looks very confusing but when you break it down into examples you begin to understand it a little bit. The first piece of my URL is the anchor component which checks the string at a particular boundary point.

^ - This is for the beginning of the expression and identifies the beginning of the string that should follow it. this anchor can be used in two different ways which signify the exact match, for example ^ABC. "ABC" and "ABCDEFG" would both be matches and to also signify a range of possible matches using bracket expressions. We will investigate bracket expressions in a later section.

### Quantifiers
In regex, quantifiers are defined as numbers of characters or expressions that matches. there are two different types of quantifiers, Gredy and lazy but they each have the same description * and *?  Matches Zero or more times.
+ and +?  Matches One or more times.
? and??  Matches Zero or One times.
{n} and {n}?  Matches exactly n times.
{n,} and {n,}?   Matches at least n times.
{n, m} and {n, m}?  Matches from n to m times.
examples of these are 1. https? Because the `? ` Matches 'https'.
[\da-z\.-] +     Because of the `+` it matches a single digit, group of letters (a-z), dot (.) or hyphen (-) 1 or more times
[a-z\.] {2,6}    Because of the ` {2,6} ` it matches 2 to 6 copies of the sequence [a-z\.]
[\/\w \. -] *     Because of the `*` it matches '/', '.', '-', 'www', '//'

### OR Operator
There are also components of regex called OR operator
'|' - Alteration which matches the expression before or after the quantifier (acts like a boolean OR)

### Character Classes
\d Matches a single character which is a digit.  for example ([\da-z\.-] +)
\w Matches any word character. Alphanumeric character plus underscore. for example [\/\w \. -]

### Flags
Commonly, regular expressions are delimited by the '/'. We see this at the beginning and end of the expression, even after the anchors that we previously discussed. It is possible to identify search criteria outside of the flags to help mark the expression as global (g), multi-line (m), or insensitive (i).

### Grouping and Capturing
The expression is four significant groups:

  /^ (https?:\/\/)? and ([\da-z\.-]+)\. and ([a-z\.] {2,6}) and ([\/\w \.-]*)*\/?$/
The first group is the optional http portion. The second group is looking for any characters that will represent a domain name, followed by a ".". Then the third group is most seen as a ".com" and which is limited to 2-6 characters. The final group is the file path or directory specification. This can be repeated any number of times and be any word.

### Bracket Expressions
The bracket expressions in this regular expression:

  [\da-z\.-] and ([a-z\.] {2,6} and [\/\w \.-]
The bracket expressions identify which portions of the expressions can be the characters within each bracket. In the initial bracket expression, for this we look for any digit, or any character a-z, or any "." or "-". kind of the same as with the last two brackets, we are looking for any or all those characters.

## Author
This Regex tutorial was created by Ama Frema. GitHub: Afrema90


