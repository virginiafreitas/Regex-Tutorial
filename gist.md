# Regular Expressions Tutorial for URL Analyzis

Regular expressions or Regex are powerful tools for manipulating and validating text. In this tutorial I will explain a specific regex that have the purpose of matching URLs. I will decompose each component of the regex and explain its role in analyzing URLs. The goal of this tutorial is to help computer science students to get familiar with the logics and syntax of regular expressions.

## Summary

Regular expressions are a sequence of characters that defines a pattern in a text. Regex are widely used in computer sciences for searching, validating and manipulating strings according to specific patterns. The regular expressions offer a powerful and flexible way to solve operations of search and substitution in texts, saving time and effort. Regex have a diversity of applications, for example: validating forms, extracting data, manipulating text and analyzing URLs.

The regular expression to be analyzed in this tutorial is `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/` which is used to validate URLs. This regex verifies is a string matches the URL pattern, including schemes like "http://" or "https://", domains like "www.example.com", paths and optional parameters.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

 - The `^` character is an anchor for the beginning of the string. It indicates where the regex should start responding in the beginning of the input string.
 - The `$` character is an anchor for the end of the string. It indicates where the regex should stop responding at the end of the input string. 

### Quantifiers

 - The `?` quantifier indicates that the previous item is optional. In this case, it refers to the "s" in "https", turning the "s" optional and allowing both "http://" and "https://".

### Grouping Constructs

 - Parentesis are used to create a group of capture. In this case the `(https?:\/\/)?` group captures the URL scheme like "http://" or "https://". The period after the group turns it into optional.

### Bracket Expressions

 - The squared brackets in `[\da-z\.-]` define a set of allowed characters. In this case, it includes digits (`\d`), lower capital characters (`a-z`), period (`.`) and hifen (`-`), which are used to capture parts of the domain, like "www".

### Character Classes

 - A class of characters like `[a-z\.]` is defined between squared brackets. In this example, the class includes only lower capital characters and a period. This is used to define the extension of the domainm such as "com" or "org".

### Flags

 - The slash `/` is used as a delimitator. It separates the regular expression from the beginning and from the end, as well as modifiers known as "flags". At the end of the expression there is a `\/?` where the slash is followed by `?`, indicating the final slash is optional.

### Character Escapes

 - At `\.` the escape character `\` is used to treat the period `.` in a literal manner. The period is a special character in regex that would normally correspond to any character, so it is important to escape it so that it corresponds only to the literal period in a domain.

## Conclusion

Understanding the URL matching regex is a great way to start to understand how regular expressions work and how they can be applied to validating and analyzing texts.

## Developer Information:
  - Virginia Freitas
  - GitHub URL: https://github.com/virginiafreitas
  - e-mail address: virginiacdefreitas@gmail.com