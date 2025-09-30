# Email Regex Tutorial

This MarkDown will be going over regular expression and how to properly format it. In this instance, for Email.

## Summary

I chose Email for this example because of how much it would be used for email verification. With most all apps wanting an email profile. Being able to verify a correctly entered email address is essential. The following is a regular expression for Email. Looking for any variety of characters acceptable in an email address (min 1), followed by an "@" (txt) and "." (txt). As per standard email format. /^[\w\.\+\*\?\^\$\/,!#&'-=~]+@\w+\.\w{2,6}$/ Forward slashes surrounding it for standard JavaScript use.

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

Anchors are used to set up the position of the syntax you are looking for. In my example ^[\w\.\+\*\?\^\$\/,!#&'-=~]+@\w+\.\w{2,6}$ the anchors are the ^ and $ signifying the start and end of the regex. Another useful anchor is \b, this signifies a word boundary. A good example for this is if you are looking for the word "I", if you were to type \bi\b than the user would return only the word "I" and not every iteration of the letter itself.

### Quantifiers

Quantifiers are used to indicate how much you are wanting returned. In my example of ^[\w\.\+\*\?\^\$\/,!#&'-=~]+@\w+\.\w{2,6}$ quantifiers are used 3 times. 2 instances of a + indicating 1 or more and {2,6} indicating anywhere from 2 to 6 characters long. Some other quantifiers are \* indicating 0 or more, ? indicating 0 or one (this is good if you wanted it to be something like "colou?r" to be able to find both variations of spelling), then there is {x} (x being a numeric variable) for a specific amount, or {x,} for a specified amount or more.

### Grouping Constructs

Grouping Constructs are used signified by parenthesis "()". This is used to group things together you want to. I do not have any in my example because it's not entirely necessary in this example. But it would still work if they were in there like such, ^([\w\.\+\*\?\^\$\/,!#&'-=~])@(\w+)\.(\w{2,6})$. This can help you understand each section as well, so feel free to use it even if not necessary.

### Bracket Expressions

Bracket Expressions are used for matching anything inside [x] or not inside [^x] brackets. In my example, ^[\w\.\+\*\?\^\$\/,!#&'-=~]+@\w+\.\w{2,6}$ inside the bracket, it can include the word character class, number, or listed symbol. Can have some bracket expressions with dashes to cover an array of letters or numbers as well. For example: [a-z] being any lowercase letter or [^A-Z] not any capital letters.

### Character Classes

Character Classes are good for covering an array of options simply. In my example, ^[\w\.\+\*\?\^\$\/,!#&'-=~]+@\w+\.\w{2,6}$, \w is used for any alphanumeric characters as well as an underscore. There is also \d for digits, \s for whitespace.

### The OR Operator

The OR Operator is extremely useful as well. A good example for this would be if we were doing a basic email search looking for a .com or a .net specifically, it could look like this: ^\w+@\w+\.(com|net)$.

### Flags

Flags are used "outside" of the regex. I say outside because they're used in JavaScript on the end of the last forward slash. Some flags being g, for global (matching all occurences). Or i, for case insensitive (ignores case when searching). With my example being ^[\w\.\+\*\?\^\$\/,!#&'-=\~]+@\w+\.\w{2,6}$, in JS with a flag for global and case insensitive, it would be written as follows const regexEmail = /^[\w\.\+\*\?\^\$\/,!#&'-=\~]+@\w+\.\w{2,6}$/gi;.

### Character Escapes

Character Escapes are extremely useful and necessary for regex. In my example they are used multiple times and are represented with the a backslash. ^[\w\.\+\*\?\^\$\/,!#&'-=~]+@\w+\.\w{2,6}$ with the first section wanting to be inclusive of multiple possible symbols within an email, the backslash is used to represent that literal character. It is also used for character classes, but you will notice the character classes will have a letter after, where if we want to use the backslash for a character escape, there is a symbol following the backslash. An example of this would look like \\*.

## Author

Thank you for taking the time to check this out. My name is Maury and my github is https://github.com/MauryIV. I had a lot of fun studying up on this to present and share this information. I hope you have found it useful. Please feel free to reach out if you have any questions.
