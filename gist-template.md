# Regular Expressions

Regular expressions are powerful tools for matching patterns in text. They are widely used in programming, data processing, and text editing. This guide explains regex components and how they can be used effectively.

## Summary

This will explain the basics of regular expressions, including anchors, quantifiers, the operator, character classes, flags, grouping and capturing, bracket expressions, greedy and lazy matching, boundaries, black-reference, look-ahead, and look-behind assertions.

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
Anchors are used to specify the position in the text where a match occurs. The `^` anchor is the the start of the line, the `$` anchor is the end of the line.

Example: `^start` matches "start" only if it is at the beginning of a line.

### Quantifiers
Quantifiers is teh number of times a character or group can occur. The `*` matches zero or more occurrences, the `+` matches one or more occurrences, and the `?` matches zero or one occurrence.

Example: `a+` matches one or more "a" characters.

### OR Operator
The Operator `|` is used to specify alternative. It matches either the expression before or after it.

Example: cat|dog matches either "cat" or "dog".

### Character Classes
Character classes match any one of a set of characters. They are defined inside square brackets `[]`

example: `[aeiou]` matches any vowel.

### Flags
Flags modify how a regex pattern is matched. the `i` flag makes the match case-insensitive, and the `g` flag performs a global match.

Example: `/pattern/1` matches "Pattern" and "PATTERN"

### Grouping and Capturing
PParentheses `()` are used for grouping and capturing subexpressions. The matched text can be refrenced later using back-references.

Example: `(abc)+` matches one or more occurrences of "abc" and captures it.

### Bracket Expressions
Bracket expressions `[]` are similar to character classes but allow specifying ranges of characters.

Example: `[a-z]` matches any lowercase letter.

### Greedy and Lazy Match
quantifiers are greedy by default, meaning the match as much text as possible. Adding a question mark `?` after the quantifier makes it lazy, matching as little text as possible.

Example: `a.*b` matches " along string of text b", while `a.*?b` matches "a b"
### Boundaries
Boundaries specify the position of a match in relation to word boundaries of other non-word characters. The word boundary `\b` matches the position between a word character and a non-word character. 

Example; `\bword\b` matches "word" as a whole word, not as part of another word 

### Back-references
Back-references `\1`,`\2`, etc., are used to match the same text as previously matched group.

example: `(cat|dog) \1` matches "cat cat" or "dog dog"

### Look-ahead and Look-behind
look-ahead `(?= )` and look-behind `(?<= )` are used to match a pattern only if it is followed by or preceded by another pattern, respectively, without including the other pattern in the match.

Example: `(?<=\$)\d+` matches one or more digits preceded by a dollar sign.

## Author

This guide was written by Bernardo Alonso. You can find more of my work on https://github.com/oneuglyghost
