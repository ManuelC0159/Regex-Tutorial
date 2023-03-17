# Regex-Tutorial
This is a tutoriial explaining the use of regex to match emauls using   `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.
This is extremly useful when validating emails specially when using things apps like Node

## Summary
A regex expression is a sequence of characters that defines a specific search pattern. In this scenario, the patter would be `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.
The pattern is ran through algorithms and code to make sure the user input is a valid email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
 Since regex are literal, they are wrapped in slash(`/`) characters. Our email validation regex follows this rule `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.
 We will start breaking the sequence down as we go through each component in more detail.
### Anchors
 The anchor characters in this regex are the `^` which signifies a string that begins with the characters after it, in otherwords, the begging of a string. The final anchor is the `$` character which marks the end of the string. Since this regex does not have the multiline flag (`m`), the `$` is followed by the `/` thus ending the sequence. 
### Quantifiers
 Quantifiers in this regex are `+` to link the big 3 parts of the email: the username + service + .com.  This allows for the algorithm to check different conditions for the different sections of the email address, allowing it to check more dynamically than if it used the same rule for the whole string of email address. The other qunatifier in this regex is the `{2,6}`, which defines the min and max range of times we want to find the squence `([a-z\.])`.

### OR Operator
 This regex does not use an OR operator!
### Character Classes
 This regex uses the character class `\d` which is the equvilant of `[0-9]`. the `\d` character class defines a set of characters to look for. for example anything inside the `[]` is considered a character class. However, there are some common character classes, such as `\d`, that make things simpler. Using `\d` instead of typing out `[0-9]` for example. `\d` also searches for numerical digits, not characters
 ### Flags
 This regex does not use any flags!
### Grouping and Capturing
 Each group in a regex is defined by the `()` characters. In this regex, for example, the groups would be `([a-z0-9_\.-]+)` , `([\da-z\.-]+)`, and `([a-z\.]{2,6})`. Again, this are for the email name, email service, and the .net or .com ending of the email.
### Bracket Expressions
 The bracket expression in this regex are `[a-z0-9_\.-]`, going from lef to right the expression checks for case sensitive letter from a-z. Then, matches characters 0-9, and `_`,`.`, `-`. 
 The second expression is `[\da-z\.-]`, which starts matching digits 0-9, case sensitive a-z, and characters `.` and `-`.
 Finally `[a-z\.]` matches case sensative a-z and `.`.
### Greedy and Lazy Match
 The email validation regex uses greedy quntifiers, which are `+` and the `{}` when matching the last group. 
## Author

My name is Manuel Camacho, alway trying to learn more in the world of programing when I can (GitHub: [ManuelC0159](https://github.com/ManuelC0159))

