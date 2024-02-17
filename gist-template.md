# Title (replace with your title)

A regular expression, or regex, is a sequence of characters used to match patterns in text. These expressions are extremely useful for extracting data like phone numbers, emails, etc that follow a specific pattern from text, and they can be used in almost any programming including JavaScript.

## Summary

In this tutorial I will break down the following regex for matching an email /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ into its basic components. This regex would be useful for validating email input in various applications.

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
This regex uses the anchors ^ which denotes the start of the string and $ which denotes the end of the string. Multiline is not enabled so the markers indicate start and end of a string as opposed to a line.
### Quantifiers
The quantifiers +, which means one or more, and {x, y} where x is the min and y is the max are used in this regex. For example, the first + means one or more characters that satisfy the requirements of [a-z0-9_\.-], the later + similarly denotes one or more characters in the group [\da-z\.-], and the {2, 6} indicates two to six characters in the group [a-z\.].
### OR Operator
The [] OR operator is used in this regex. For example, [a-z0-9_\.-] means any character a-z (case insensitive), any digit 0-9, _, ., or -. The \ is used to denote a literal . instead of the usual meaning of . which is "any character".
### Character Classes
This regex uses the character class \d which denotes any digit character 0-9. The \ indicates the character class which is distinct from a plain d meaning literally the letter d.
### Flags
The regex is enclosed by two / characters with no flags. Since multi-line is not enabled (by following the ending / with an m), the anchors match a string instead of the start and end of a line.
### Grouping and Capturing
In this regex, () parentheses are used to capture a group. The first set of () captures the username of the email address, the second set captures the domain name, and the final set captures the domain. Broken down, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ means one or more characters a-z (case insensitive), 0-9, _, ., or -, followed by a literal @, followed by one or more characters of any digit 0-9, a-z (case insensitive), ., or -, followed by a literal ., followed by 2-6 characters a-z (case insensivite) or ..
### Bracket Expressions
Using brackets allows a regex to match specific characters in a range. So, [a-z] is not looking for a or - or z, but actually looking for any letters a through z. And in the brackets the "-" is not taken literally in the cases of a-z or 0-9. But after the \ to escape the period it is recognized as a literal "-".
### Greedy and Lazy Match
A greedy match will match as much as possible while the lazy match will try to match as little as possible. In matches in the email regex are greedy and will match as much as possible.
### Boundaries
Regex boundaries are placeholders that match a specific position in a string rather than matching a character. They don't match any actual characters but rather the spaces between characters or between a character and the start or end of a string. Regex boundaries are useful for defining where certain patterns should start or end within a string. Here are some commonly used boundaries:
### Back-references
In the regular expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, there are no explicit back-references defined using \1, \2, etc. Back-references are used to refer to previously captured groups within the regex pattern. However, in this particular regex pattern, there are no such back-references.
### Look-ahead and Look-behind
This regular expression doesn't use look-ahead or look-behind assertions. Instead, it matches the entire email address pattern from start to end, capturing the local part, domain name, and TLD into separate capturing groups.
## Author

My name is Kevin Hunt, and I'm a UCF Bootcamp web developer in training. My github is https://www.github.com/kvnhunt . Please also feel free to email me at huntk.twitch@gmail.com.
