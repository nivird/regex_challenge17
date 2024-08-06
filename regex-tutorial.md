# Title (Regex Expression Tutorial)
Regular expressions (regex) are powerful tools for matching patterns in strings. This tutorial will break down a specific regex designed to match URLs. By the end, you'll understand how each part contributes to the overall pattern.

## Summary

The regex we will be discussing is used to match URLs. Here's the regex:

regex
Example code:
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
This regex can validate URLs that start with "http://" or "https://", followed by a domain name, and optionally include a path. We'll break down each component to explain how it works.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors are used to specify the position of the match within the string.

1. ^ asserts the position at the start of the string.
2. $ asserts the position at the end of the string.
In our regex:
example code:
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
3. ^ ensures the match starts at the beginning of the string.
4. $ ensures the match ends at the end of the string.

### Quantifiers

Quantifiers specify how many instances of a character or group must be present in the input for a match to be found.

1. ? matches 0 or 1 time.
2. * matches 0 or more times.
3. {2,6} matches between 2 and 6 times.
Example code: 
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
4. https? matches "http" or "https".
5. (https?:\/\/)? matches "http://" or "https://" at the start of the string or no protocol.
6. {2,6} ensures the domain extension is between 2 and 6 characters long.
7. ([\/\w \.-]*)* matches the path of the URL, including /, alphanumeric characters, spaces, dots, and hyphens, 0 or more times.
8. \/? matches the trailing slash at the end of the URL, which is optional.
### Grouping Constructs
Grouping constructs are used to group parts of a regex together.
Example code:
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
1. (https?:\/\/)? groups the protocol part.
2. ([\da-z\.-]+) groups the domain name.
3. ([a-z\.]{2,6}) groups the domain extension.
4. ([\/\w \.-]*)* groups the path part.
### Bracket Expressions
Bracket expressions (also called character classes) match any one of the enclosed characters.
Example Code
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
1. [\da-z\.-] matches any digit, lowercase letter, dot, or hyphen.
2. [a-z\.] matches any lowercase letter or dot.
3. [\/\w \.-] matches any forward slash, word character (alphanumeric), space, dot, or hyphen.

### Character Classes
Character classes are shorthand for common sets of characters.
Example Code
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
1. \d matches any digit.
2. \w matches any word character (alphanumeric plus underscore).
### The OR Operator
The OR operator (|) allows for matching one pattern or another. In our regex, it is not explicitly used, but s? effectively acts as an OR operator to match "http" or "https".
### Flags
Flags are optional parameters that modify the behavior of the regex. In our example, there are no flags used, but common flags include:

i for case-insensitive matching.
g for global matching (find all matches rather than stopping after the first match).
m for multi-line matching.

### Character Escapes
Character escapes allow special characters to be treated as literal characters.
Example code:
‟/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/”
1. \/\/ matches a literal forward slash.
2. \. matches a literal dot.
## Author

I am a web development student passionate about learning and sharing knowledge about programming. You can find more about my work on https://github.com/nivird


