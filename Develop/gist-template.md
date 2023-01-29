# Regex Tutorial: Matching An Email

This tutorial will take you through the various regular expressions that make up the string that allow us to search for email through text and variables.

## Summary

Matching email regex:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The following text describes the regular expression that is used to search for email addresses.

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

This regex features two anchors in both the `^` and `?` characters.

These two work together in that the caret (`^`) denotes the beginning of a line or string. In our example, the `^` opens the regex as a string of text that will eventually be an email address. When the logic is complete, the string is closed using the question mark (`?`) character. It's really that simple!

### Quantifiers

Quantifiers (`*, +, ?, {}`) specify how many instances of a character, group, or character class must be present in the input for a match to be found.

`([a-z0-9_\.-]+)` The `+` in this captured group means that the characters that precede it can match one more times.

`([\da-z\.-]+)` The `+` in this captured group means that the characters that precede it can match one more times.

`([a-z\.]{2,6})` The `{2,6}` in this captured group means that no less than 2 characters will be accepted but no more than six based on the regex defined.

### Grouping and Capturing

Capturing groups (`()`) use parentheses to treat multiple characters as a single unit. In this example, these parentheses wrap around our previous character classes and include a bit more information to treat each set of characters as a specific portion of the email template.

`([a-z0-9_\.-]+)` This captured group creates the expression for the email name.

`([\da-z\.-]+)` This captured group creates the expression for the email provider or the domain.

`([a-z\.]{2,6})` This is the last captured group in the expression which is the extension group.

### Bracket Expressions

A list of characters enclosed within square brackets (`[]`). Bracket expressions match single, or a range, of characters in a list.

`[a-z0-9_\.-]` The first bracket expression in the regex that specifies the email name can contain letters a-z and numbers 0-9. They will be followed by a period. That period represents nothing else in this context.

`[\da-z\.-]` Much like the string above, this bracket expression is letting us know that any digit and characters between a-z are accepted for this email domain. This is followed, of course, by a single period being used as an actual period in this instance.

`[a-z\.]` This is the last bracket expression section found within our Match and Email regex. This represents the extension group portion and shows that only characters between a-z will be included. No numbers this round and this extension is, of course, followed by a period.

### Boundaries

In this regex, we have both boundaries (`^, ?`) and anchors (`^,?`). They both work similarly in that they indicate the beginning and ending of a string but boundaries come from a slightly different angle and ensure that to the left of this `^` there cannot be anything else.

## Author

This tutorial was created by student H. Their github can be found [here](https://github.com/hkorczynski).
