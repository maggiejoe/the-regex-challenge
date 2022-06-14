# The Regex Challenge

Introductory paragraph (replace this with your text)

## Summary

In this challenge I will explain how the following Regex is used to match Hex Values. 

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

If you aren't familiary with Hex Values, they are values used to display specific color(s). It is broken down into three sets of 1-3 digits per set. For example, the following Hex Values describe the color green 

(0, 128, 0)

As you go through this gist, you'll learn how the Regex expression above works to find any Hex Values.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Anchors 

Anchors do not match any characters but rather say something about a string or what follows.

Anchor: `^`

    This anchor identifies the beginning of a string of data

    For example: `^The` means that the string must begin with `The`

    In the case for finding HEX values, the `^#` means that the beginning of the string must match the character #. The # is used to indicate the differences between hexadecimal and decimal numbers which is very important with HEX values. 

    If you're unsure of the differences of hexadecimal and decimal numbers, use the following link below for more details.

    [Hexadecimal vs Decimal Numbers](https://www.schoolelectronic.com/hexadecimal-vs-decimal/)

Anchor: `$`

    This anchor is very similar to the `^` however instead of identifying the beginning of a string, it identifies the end

    For example: `end$` means that the string must end with `end`

### Quantifiers

A quantifier specifies how many times a character or group of characters must be present in a specific input in order to find a match. 

Quantifier: `?`

    The `?` is used to describe a boolean by using 0 or 1 (true, or false). By using the `?`, it makes the character or symbol coming before it is optional.

    For example: `Plants!?` will match either `Plants` or `Plants!` 

    In our Regex, the `?` following the `#` means that the `#` is optional and may or may not be needed at the beginning of the expression.

Quanitfier: `{}`

    The `{}` around a number indicates that the preceeding code should happen x amount of times.

    For example: `a{3}` matches a string of `aaa`.

    In the HEX values Regex the `[a-f0-9]{6}` indicates that the expression in the `[]` must have 6 instances of that string. In the `[a-f0-9]{3}` expression, the `{3}` indicates that the expression preceeding it must have 3 instances of that string. In both expression in the `[]`, we now understand that the quantifier will allow each expression to happen either 6 or 3 times using the characters a-f and/or numbers 0-9.

### OR Operator

OR Operator: `|`

    Similar to the OR operator in JavaScript `||`, it means that it will match the characters or expressions on either the left or right side of the `|`.

    For example: `hello|HELLO` will match either `hello` or `HELLO` from the string.

    In our Regex, this means that it will match either a 6 character string with the characters of a-f and/or 0-9 OR a 3 character string with the characters a-f and/or 0-9. Anthing that does not match 6 or 3 characters will not match the Regex.

### Flags

Flags use the `/`, forward slash symbol at the beginning and end of the Regex.

Flags are what holds the Regex together and tells the finder what to look for between these two characters.

### Grouping and Capturing

Grouping and Capturing is a way of treating multiple characters as a single unit.

Grouping/Capturing: `()`

    The `()` is used to bring all of the characters within the parenthesis into a single array

    For example: `(hello)` brings the single characters `h`, `e`, `l`, `l`, `o` together into a single group

    In our Regex, the `([a-f0-9]{6}|[a-f0-9]{3})` is putting the values between the parenthesis together. What is happening between them is described in more detail throughout this document

### Bracket Expressions

Bracket Expression: `[]`

    The expression `[]` is used to combine any characters (symbols, alphabetic, numeric, special characters...etc.) within the brackets.

    For example: `[a-f0-9]` in our regex is combining the combination of letters a-f and numbers 0-9 into one string. The hypen between the `a-f` and `0-9` indicates the range from once character to the other. Meaning any number including `0` and up to and including `9`, and any letter including `a` and upto and including `f`.

### Greedy and Lazy Match

A Greedy match means match the longest possible string. A Lazy Match means match the shortest possible string. 

For example: `h.+l` matches the `hell` in `hello` but `h.+?` matches the `hel`.

We know that normal quantifies such as the `{}` in our Regex are greedy, meaning that the regex will match as many possible occurances of the specific pattern preceeding it. If our expression had a `?` then it would become a lazy match and would match the fewest possible occurances of the specific pattern preceeding it. 

In the case of our Regex, we know that it is greedy.

## Author

Hey! My name's Maggie! I'm an aspiring junior developer currently working through the University of Toronto Coding Bootcamp. After this course is done I look forward to adding to a well rounded portfolio and creating fun and new applications that inspire me!

In my free time I enjoy caring for my many many house plants and spending as much time outdoors as possible. As I'm currently writing this, I'm sitting outside sipping on a tea. 

If you'd like to learn more about me and see the work I've done up until this point, feel free to checkout my GitHub link below!

Can't wait to connect with you!

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

https://github.com/maggiejoe