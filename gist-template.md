# Regex Tutorial

Regular expressions (regex) are powerful tools for pattern matching and string manipulation in programming. One of the most common tasks is validating email addresses, which is essential in many applications. In this tutorial, we'll break down a regex used to validate email addresses and explain each component in detail.

## Summary

In this tutorial, we will explore a regular expression that validates email addresses. The regex we'll discuss is:

^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$

We will explain each part of the regex, including anchors, quantifiers, character classes, and more, to give you a comprehensive understanding of how this pattern works.

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

### Anchors

- ^: This anchor ensures that the match starts at the beginning of the string. It prevents partial matches within a string.
- $: This anchor ensures the match ends at the end of the string. It guarantees there are no trailing characters after the email address.

### Quantifiers

- +: This quantifier matches one or more occurrences of the preceding element. For example, [a-zA-Z0-9._%+-]+ means the user part of the email (before the @) must consist of one or more of the characters defined in the character set.

### OR Operator

- This regex doesn't explicitly use the OR (|) operator, but if we were to allow multiple domains (like gmail.com or yahoo.com), we could use it like so: (gmail|yahoo)\.com.

### Character Classes

- [a-zA-Z0-9._%+-]: This character class matches any letter, digit, or specific special characters (., _, %, +, -). These characters are allowed in the username of an email address.
- [a-zA-Z]: This class ensures that the domain’s top-level domain (TLD) consists only of letters (e.g., com, net, org).

### Flags

- This regex does not use any flags, but common flags include i (case-insensitive) and g (global search).

### Grouping and Capturing

- This particular regex does not use parentheses () for grouping or capturing, but grouping can be used to extract specific parts of a match or apply operators to multiple characters.

### Bracket Expressions

- [a-zA-Z0-9._%+-]: The bracket expression matches any one character inside the brackets. It includes a range for lowercase letters (a-z), uppercase letters (A-Z), digits (0-9), and special characters (., _, %, +, -).

### Greedy and Lazy Match

- Greedy match: The quantifier + is greedy, meaning it tries to match as many characters as possible. In this case, it matches all valid characters in the username and domain parts of the email.

### Boundaries

- The start (^) and end ($) anchors act as boundaries, ensuring the regex matches the entire string and not a part of it.

### Back-references

- This regex does not use back-references, which refer to previously captured groups.

### Look-ahead and Look-behind

- This regex does not use look-ahead or look-behind assertions, which are used to assert that a string is followed or preceded by a specific substring.

## Author

This tutorial was created by  [Christopher Chhim](https://github.com/Christopher-Chhim). Check out more of my projects on GitHub!  

## Gist Link

For a full breakdown of the regex tutorial please check out my gist here:
(https://gist.github.com/Christopher-Chhim/818b7e005853e45d03bc378086f95c65)