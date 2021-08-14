# RegEx Tutorial

In this tutorial you will be learning what RegEx/regular expression can do. In particular how to "Defang" a URL or IPv4 address. This particular method is one of the most sought out codes for RegEX. As well as learning the basic of RegEx such as anchors, quantifiers, grouping constructs and etc.

## Summary

Regular expression (Regex) allows one to use a series of particular characters that interprets a search pattern. That is paired with code or algorithms. As you read I will be breaking down the basic functions of Regex and how I used it to “Defanged” URL or IPv4 address.




## Table of Contents

- [](#)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components
All patterns must be wrapped in slash characters `/`.
Just as you see in the code below.

`/^(((h..ps?|f.p):\/\/)?(?:([\w\-\.])+(\[?\.\]?)([\w]){2,4}|(?:(?:25[0-5]|2[0-4]\d|[01]?\d\d?)\[?\.\]?){3}(?:25[0-5]|2[0-4]\d|[01]?\d\d?)))*([\w\/+=%&_\.~?\-]*)$/`

(“Defanged” URL or IPv4 address - replaces every period `"."` with `"[.]"` )

### Anchors
These character `^` and `$` are called anchors. Where `^` anchor means a string that begins with the character that follow it. It is important to note that regex is case sensitive, so if we had ^Apple it will look for exact string matches like "Apple" or "Apple sauce". This would have not work if the A in apple was lowered cased.

As for `$` anchor signifies a string that ends with the character that precede it. Just as we saw in the Defanged URL/IPv4 address code the string must start and end with something that matches the pattern.


### Quantifiers

Quantifiers impose limits of the string that your regex corresponds to. A lot of the time, they include the minimum and maximum number of characters that your regex is seeking. That being said, quantifiers have many occurrences of particular patterns. Such as:

*—Matches the pattern zero or more times

+—Matches the pattern one or more times

?—Matches the pattern zero or one time

{}—Curly brackets can provide three different ways to set limits for a match:

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

### Grouping Constructs

The "Defanged" code shown above, is a prime example of how grouping constructs are used.The main way you group a section of regex is by using parentheses as shown in part in this small code of Defanged.

`([\w\-\.])`

### Bracket Expressions
 represent a range of characters that we want to match inside a set square bracket `([])`. Bracket expressions are also known as positive character group because they outline the characters we want to include.

### Character Classes

A set of characters is defined by a character class in a regex. The most common character classes are

. —Matches any character except the newline character (\n)

\d —Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

\w —Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). 

\s —Matches a single whitespace character, including tabs and line breaks

### The OR Operator
Not all bracket expression are need to meet the requirements in a string pattern. Normally used for when grouping construct or between two different grouping constructs.

The OR operator `(|)`, can be used as such `[R|e|g|e|x]` which can also be written as `[Regex]`. All depends on what you want to group or keep separate.

### Flags
Define additional functionality or limits for the regex. Below are some example that we are more likely to use or encounter in regex

g—Global search: the regex should be tested against all possible matches in a string.

i—Case-insensitive search: case should be ignored while attempting a match in a string

m—Multi-line search: a multi-line input string should be treated as multiple lines

### Character Escapes

If you wanted a character to not be interpreted as literal then adding a backslash `\` allows the character to escape. Meaning that if we had a `{` normally regex would see this as a quantifier but if were to add a backslash `\{` regex is now only looking for a open curly brace; instead of viewing it as a quantifier. 


## Author
If you wanna see more of my work feel free to check out my GitHub profile https://github.com/Thetodd7
