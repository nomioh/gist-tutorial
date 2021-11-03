# Gist Tutorial: Matching an Email

Regular Expressions can be complex but they are flexible and powerful and can be used to perform comparisons and validate.

## Summary

In this tutorial I will be showing how to validate an Email using this RegEx. This regex matches an email and can be used to find email addresses within a string of text and verify if the email is valid.

    `/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

We will be taking a closer look at all of the components of this string seperatly to understand it better. A regular expression contains basic components such as anchors, quantifiers, OR operators and bracket expressions.

### Anchors

The `^` and `$` in the regex string are the anchors, they mark the beginning and the end of the expression.

The starting anchor `^` is used to match any string that follows the anchor. For example `^Welcome` would match a string that starts with the word `Welcome`.

The ` $` end anchor matches right after the last character in the string.

In our regex, the anchors are indicating that the match up must match the characters that are defined by the expression located within the beginning and end anchors.
`([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})`
Let's disect this expression further!

### Quantifiers

Quantifiers are used to indicate ranges in the number of occurence, the two quantifiers are: + operator and {2,6}
One of the quantifiers are the curly brackets `{}` in this regex, In this instance the `{2,6}` which means that we need to find the string patterin a min of two times and a maximin of 6 times. The email string can be between 2 and 6 characters.

### OR Operator & Bracket Expressions

The `[]` square brackets indicate that the search will match any character that is listed within the brackets.
Our regex example has two OR Operators. The first one is `[a-z0-9_.-]` which indicated that any letter from a-z, any number from 0-9 or a dot, dash would return a match.
The second OR Operator in the regex is `[\da-z.-]`, this indicates that any digit "/d" or letter from a-z or a dot or dash could return a match. This regex pertains to the ".com" part of the email address.

### Character Classes

Character classes define sets of characters.
`/d` matches a single non digit character

### Flags

Placed at the beginning and the end of the RegEx `\\`: `/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/`

Regex are contained with flags/slashes to limit the search

### Grouping and Capturing

Parentheses are used in regular expressions to group together parts of the search. Our regex is grouped into three parts. The first grouping is to define the characters that are found before the @ in an email address: `([a-z0-9_.-]+)`. It can contain letters, numbers, dots or hyphen.
The second grouping; `([\da-z.-]+)` is used to define the characters after the "@" in the email address for example, gmail, outlook, hotmail etc.
The third grouping `([a-z.]{2,6})` is used to define the domaine characters that come after the . in an email address, for example com, ca, ru etc

### Greedy and Lazy Match

The quantifiers `* + {}` are greedy operators, they match for any character as many times as needed so that a character could be matched even if it is used more than once. We see this in our regex twice `([a-z0-9_.-]+)` & `([\da-z.-]+)`

## Author

Noyemi Ohanyan is a Full Stack Developer from Toronto, currently studying at the University of Toronto Coding Bootcamp. (https://github.com/nomioh)
