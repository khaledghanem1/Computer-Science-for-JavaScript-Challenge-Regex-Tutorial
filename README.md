# Regex-Tutorial 

In this tutorial were going to dive into regex, explaining some of its components to upcoming developers. This tutorial is made to students to simplfy search pattern of regex. Clicking on the links in the table of contents will show you a detailed explantion of the component. 
<br>

## Summary
Regular expressions, or regex for short, are a series of special characters that define a search pattern. Take the following example of a regular expression, which we’ll call “Matching a Username”:
```
/^[a-z0-9_-]{3,16}$/
```
<br>

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
<br>

## Regex Components
<br>

### Anchors - ^ and $
Both ^ \$ are considered to be Anchors
The character after the anchor denotes the beginning of a string
A string that ends with the characters before it is denoted by the $ anchor. It can be preceded by an exact string or a range of potential matches, much like with the character.
<br>

### Quantifiers - * + ? and {}
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for.

Quantifiers are inherently greedy, meaning they match as many occurrences of particular patterns as possible. They include the following:

| Syntax      | Description |
| ----------- | ----------- |
| \*      | Matches the pattern zero or more times       |
| \+   | Matches the pattern one or more times        |
| \?   | Matches the pattern zero or one time        |

Curly brackets can provide three different ways to set limits for a match:

| Syntax      | Description |
| ----------- | ----------- |
| { n }   | Matches the pattern exactly n number of times        |
| { n, }   | Matches the pattern at least n number of times        |
| { n, x }   | Matches the pattern from a minimum of n number of times to a maximum of x number of times        |


Each of these quantifiers can be made lazy by adding the ? symbol after it, meaning it will match as few occurrences as possible.
<br>

### OR Operator - | or []

| Syntax      | Description |
| ----------- | ----------- |
| a(b\|c)    | matches a string that has a followed by b or c (and captures b or c)        |
| a[bc]    | same as previous, but without capturing b or c        |
<br>

### Character Classes - \d \w \s and .

| Syntax      | Description |
| ----------- | ----------- |
| \d    | matches a single character that is a digit        |
| \w    | matches a word character (alphanumeric character plus underscore)        |
| \s    | matches a whitespace character        |
| .    | matches any character     |

***Use the . operator carefully since often class or negated character class (which we’ll cover next) are faster and more precise.**
<br>

### Flags

A regex usually comes within this form /abc/, where the search pattern is delimited by two slash characters /. At the end we can specify a flag with these values (we can also combine them each other):

| Syntax      | Description |
| ----------- | ----------- |
| g (global)    | does not return after the first match, restarting the subsequent searches from the end of the previous match        |
| m (multi-line)    | when enabled ^ and $ will match the start and end of a line, instead of the whole string        |
| i (insensitive)   | makes the whole expression case-insensitive (for instance /aBc/i would match AbC)        |


<br>

### Grouping and Capturing — ()

This operator is very useful when we need to extract information from strings or data using your preferred programming language. Any multiple occurrences captured by several groups will be exposed in the form of a classical array: we will access their values specifying using an index on the result of the match.

| Syntax      | Description |
| ----------- | ----------- |
| a(bc)    | parentheses create a capturing group with value bc       |
| a(?:bc)*     | using ?: we disable the capturing group |
| a(?\<foo>bc)      | using ?<foo> we put a name to the group  |


### Bracket Expressions — []

| Syntax      | Description |
| ----------- | ----------- |
| [abc]     | matches a string that has either an a or a b or a c -> is the same as a|b|c       |
| [a-c]   | a string that represents a single hexadecimal digit, case insensitively |
| [a-fA-F0-9]      | a string that represents a single hexadecimal digit, case insensitively  |
| [0-9]%      |  a string that has a character from 0 to 9 before a % sign |
| [^a-zA-Z]     | a string that has not a letter from a to z or from A to Z. In this case the ^ is used as negation of the expression  |

## Author

Khaled Ghanem is a Full-Stack Web Developer and Quality Assurance Analyst. He is constantly intrigued with technology and always wants to learn more and share his knowledge with everyone. Feel free to connect with him on Github or LinkedIn!

- [Github](https://github.com/khaledghanem1)
- [LinkedIn](https://www.linkedin.com/in/ghanemk/)