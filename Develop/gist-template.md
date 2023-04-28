# Title (Regular Expression Tutorial)
## Introduction
Regular expressions, or regex, are a powerful tool for matching patterns in text. One common use case for regex is to match email addresses. In this tutorial, we will break down the components of an email regex and explain how they work together to match valid email addresses.

## Summary

We will learn about matching an email regex /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ We start by understanding the purpose of a regex and why it's important in web development. Then, we discuss the structure of an email address and the different components that make up an email address.

Next, we break down the email regex pattern into its different components, such as anchors, quantifiers, OR operator, character classes, flags, grouping and capturing, bracket expressions, greedy and lazy match, and boundaries. We explain what each component does and how it contributes to the email regex pattern.

Finally, we will go through some common use cases for email regex patterns and how they can be used in real-world scenarios. By the end of this tutorial, you should have a good understanding of how to create and use email regex patterns in your web development projects.

## Table of Contents 

- [Title (Regular Expression Tutorial)](#title-regular-expression-tutorial)
  - [Introduction](#introduction)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Common Use Cases](#common-use-cases)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
    - [Boundaries](#boundaries)
  - [Author](#author)

## Common Use Cases
Regex is used in a variety of web development tasks, including form validation, string manipulation, and search and replace. Some common use cases of regex include:

Email validation
Password validation
Extracting data from a string
Validating URLs
Finding and replacing text
## Regex Components

### Anchors
Anchors are special characters that match a specific position in the input string, rather than matching a character. They are used to specify where a match must occur within the string.

The most commonly used anchors are the caret (^) and the dollar sign ($). The caret matches the beginning of a string, and the dollar sign matches the end of a string.

Example:

^user@example.com$

This regex will match only if the entire string is user@example.com. The caret ensures that the match starts at the beginning of the string, and the dollar sign ensures that the match ends at the end of the string.
### Quantifiers
Quantifiers allow you to specify how many times a character or a group of characters should be matched. Some of the most commonly used quantifiers are:

*: matches zero or more occurrences of the preceding character
+: matches one or more occurrences of the preceding character
?: matches zero or one occurrence of the preceding character
{n}: matches exactly n occurrences of the preceding character
{n,}: matches n or more occurrences of the preceding character
{n,m}: matches at least n and at most m occurrences of the preceding character
For example, the pattern /a+/ will match any string that contains one or more "a" characters, while the pattern /a{2,4}/ will match any string that contains between 2 and 4 "a" characters.
### OR Operator
The OR operator (|) allows you to match one of several possible patterns. For example, the pattern /hello|world/ will match any string that contains either the word "hello" or the word "world". In the email regular expression, we do not use the OR operator.
### Character Classes
Character classes allow you to match any character from a predefined set. Some of the most commonly used character classes are:

\d: matches any digit (equivalent to [0-9])
\w: matches any word character (equivalent to [A-Za-z0-9_])
\s: matches any whitespace character (equivalent to [ \t\r\n\f])
.: matches any character except newline
For example, the pattern /\d{3}/ will match any string that contains a sequence of three digits.
### Flags
Flags are used to modify the behavior of a regex. They are added to the end of the regex and are preceded by the letter "i" (case-insensitive), "g" (global), or "m" (multiline).

Example:

/[a-z]+/i

This regex matches any string that contains one or more lowercase letters, regardless of their case.
### Grouping and Capturing
Grouping and capturing allow you to group a pattern together and capture the matched substring. They are denoted by parentheses ().

Example:

([a-z]+)@([a-z]+).([a-z]{2,3})

This regex matches any email address that contains only lowercase letters in the username and domain name, and the top-level domain has 2 or 3 lowercase letters. It also captures the username, domain name, and top-level domain in separate groups.
### Bracket Expressions
Bracket expressions, also known as character classes, allow you to match any one character from a set of characters. For example, the regular expression [abc] would match any single character that is either 'a', 'b', or 'c'.

In the context of an email address regex, you could use a bracket expression to match any of the allowed characters in the username or domain name. For example, to match an email address where the username can only contain lowercase letters, you could use the following regex:

^[a-z]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
### Greedy and Lazy Match
By default, regex patterns are "greedy", meaning they will match as much of the input as possible. To make a pattern "lazy", you can append a question mark (?) to a quantifier. This will match the minimum number of characters possible.

Example:

/.+/

This regex matches any string with one or more characters.

/.+?/

This regex matches any string with one or more characters
### Boundaries
The email regex pattern uses the caret (^) and dollar sign ($) anchors to signify the beginning and end of the string, respectively. This ensures that the entire string matches the email address pattern and does not contain any additional characters.

## Author

Adrian is a web developer with a passion for creating efficient and effective web applications using the latest technologies. You can find more of my work on https://github.com/adriansbruno.
