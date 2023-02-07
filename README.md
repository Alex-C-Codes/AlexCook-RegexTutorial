# AlexCook-Email Address Regex Tutorial

Regular expressions, or regex, are a series of characteers that define a search pattern. With regex, we can search a string to see patterns within the string. With this README, we will explore all of the components of a regex code that is used to verify if a user's input is a valid email address.

## Summary

This regular expression (regex) is used to verify that user input is a valid email address:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Within this README, we will explain the components around how this regex code's components are used to verify that the input is a valid email address.

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

Within our regex, we have the ^ anchor and the $ anchor. 

The ^ anchor signifies a string that begins with the charracters that follow it. Since our code uses square brackets, there is a range of possible matches. In our regex, the string must begin and end with a pattern that includes lowercase letters "a" through "z," any number from "0" to "9", or inculudes these characters: "_", "\", ".", or "-". These characters can be in any order.

The $ anchor matches the end of input and will match immediately before a line break character.

### Quantifiers

The following characters include the quantifiers for our regex: `+` and `{}`.

The `+` quantifier matches the pattern one or two times. In our regex, the "+" quantifier matches the string pattern that's before the @ sign in the email.

The `{}` quantifier matches the from a minimum of 2 times to a maximum of 6 times. In this case, this means the third subexpression bracket must have 2 to 6 characters.

### OR Operator

The OR Operator is represented with a `|` and matches either the element on the left side of the operator or on the right side of the operator. This regex does not have an OR Operator.

### Character Classes

Character classes define sets of characters. Here are character classes within the regex:
- `\d` matches any Arabic numeral digit. The character class appears within a bracket and parantheses after the @ symbol and means that the regex will match with any number 0-9.

### Flags

Flags are placed at the end of a regex, after the second slash. They define additional functionality or limits for the regex. Our regex does not have a flag; however, common flags include:
- `g` -- Global search: the regex should be tested for all possible matches within a string
- `i` -- Case-sensitive search: case should be ignored while attempting to match with a string
- `m` -- Multi-line search: a multi-line input string should be treated as multiple lines

### Grouping and Capturing

Grouping constructs are used to break up sections so as to check multiple parts of a string with more complex regular expressions. Parantheses `()` are the primary way to group a section of regex. Our code has three subexpressions. The code is broken out, with each subexpression listed numerically.

1. `([a-z0-9_\.-]+)` - this checks the string before the @ sign
2. `([\da-z\.-]+)` - this checks the string after the @ sign
3. `([a-z\.]{2,6})` - this checks the string after the period "."

Each of these grouping constructs are capturing groupings since they do not have these characters "?:" at the beginning of each expression within the parantheses. This means that these capturing groups capture the matched character sequeces for possible re-use.

### Bracket Expressions

Anything within square brackets "[]" represents a range of characters that we want to match. Our expression has three bracket expressions:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

1. `[a-z0-9_\.-]` -- this bracket expression will look for all of the lowercase letters from a throuh z, all of the numbers from 0 to 9, an underscore "_", period ".", or hyphen "-".
2. `[\da-z\.-]` -- this bracket expression will search for any number 0-9 as well as any lowercase letter a through z. This will also search for a period "." and dash "-".
3. `[a-z\.]` -- this brack expression will search for any lowercase letter a through z as well as any period "."

### Greedy and Lazy Match

Quantifiers are inherently greedy, which means they will match with as many occurences of particular patterns as possible. All of our quantifiers are greedy, which include the `+` and the `{}` characters.

### Boundaries

Boundaries, shown as `\b`, allow you to search for whole words only in the form of `\bWORD\b`. This regex code does not have boundaries.

### Back-references

Backreferences allow us to refer to a previously matched regular expression. They are written as "\1". This regex does not have a backreference.

### Look-ahead and Look-behind

Lookahead and lookbehind components allow us to find matches for a pattern that are followed or preceded by another pattern. 

The syntax for lookahead is `X(?=Y)` and means wee are looking for X, but match only if followed by Y.

The syntax for lookbehind is `(?=Y)X` and means we are looking for X, but match only if the Y pattern is in front.

There are neither lookahead nor lookbehind components within our regex code.

## Author
- Name: Alex Cook
- About: Fullstack Web Developer
- GitHub Profile Page: https://github.com/Alex-C-Codes
- Email Address: alexcook1613@gmail.com