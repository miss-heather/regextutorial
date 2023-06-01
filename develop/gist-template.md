# Title (replace with your title)

This tutorial will review a regex that specifies password allowences.

## Summary

The regex we will be reviewing will require a password to include upper case and lower case letters, at least one digit, at least one special character, and be at least 8 characters long, but no longer than 20:

const regex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&]).{8,20}$/;


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
The anchors in this string include ^ at the beginning, and $ at the end. The caret (^) ensures that the password is at the beginning of the line of the string, whereas the the dollar sign ($) ensures the password ends at the end of the line of the string. 

### Quantifiers
The quantifiers in this string are the 8 and 20: .{8,20} and establish that the password must be a minimum of 8 characters and maximum of 20, with the preceding period (.) ensuring the matching of any sequence of characters align with these coding requirements.

### Grouping Constructs
The "?=..." is a positive lookahead. This is the assertion that the upcoming pattern matches without consuming the characters. In this case,(?=.*[a-z]) and (?=.*[A-Z]) ensures that there is at least one lowercase letter and one uppercase letter, respectively; (?=.*\d) ensures there is at least one digit, and (?=.*[@$!%*?&]) ensures at least one special character is included.

### Bracket Expressions
As mentioned above, the "?=..." is a positive lookahead, so in this case, using the example '(?=.*[a-z])', the bracket expression is '[a-z], which represents any lowercase letters, covering the entire alphabet. This same pattern applies throughout the aforementioned string. 

### Character Classes
Positive lookahead assertions enforce character classes in the string, ensuring that the string contains at least one of each outlined character as defined within the Grouping Constructs section. For example '[a-z]' - this character class matches any lowercase letter from 'a' to 'z', and so on, until a minimum of 8 characters is met, but no more than 20. 

### The OR Operator
This specific regex is not using an OR Operator; it is using a combination of positive lookahead assertions that enforce multiple conditions at the same time:
(?=.*[a-z]) to ensure a lowercase letter;
(?=.*[A-Z]) to ensure an uppercase letter;
(?=.*\d) to ensure at least one digit;
(?=.*[@$!%*?&]) to ensure a special character (character must be one listed within the string, so @$!%*?& can be used, but nothing else);
.{8,20} ensures a minimum of 8 characters, but a maximum of 20. 

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
