# Title Regex Tutorial

As a University of Toronto Bootcamp student, I am learning about Regular Expressions (regex). This tutorial will help breakdown one such Regex and define it so we can better learn how it functions.

## Summary

A Regular Expression is a sequence that picks out match patterns in text. Often used by string-searching algorithyms to find or find and replace operations to validate user input.

Below is a Regex that scans a string and validated whether or not it is in the format of an email address:

`^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`

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

Anchors defines the position of the pattern in the input string, not a character.

    - `$` matches after the last character (in abc, ^a is true, but ^b is not because it is not the first character)
    - `^` matches before the first character (in abc, c$ is true, but 1$ is not because it is not the last character)

In this regex:

- `^` defines the beginning of the string
- `$` defines the end of the string

Using both ensures the string matches the pattern.

### Quantifiers

Quanitifiers define how many times a character or group

- `*` matches 0 or more times
- `+` matches 1 or more times
- `?` matches 0 or 1 time
- `{n}` matches n times
- `{n,}` matches at least n times
- `{n, m}` matches from n to m times

  In this regex:

  - `+` means one or more occurrences.
  - `2,` means two or more.

### Grouping Constructs

Grouping Constructs are used to group multiple parts of the pattern together.

- `()` are used to group sections of the expression on either side of the `@`.

  In this regex:

### Bracket Expressions

Bracket Expressions are patterns specified within `[]` Brackets. If a `^` is placed at the beginning of the bracket expression it means the character can be anything except the expression within the brackets.

    - `[[:digit:]]` matches any digit

    In this regex:

- N/A

### Character Classes

Character Classes are more specific patterns encased in `[]` Brackets. It specifies characters that will match a single character from a set. They match any single character contained thin the set within the `[]` .

    - `[aeiou]` matches any vowel
    - `[0-9]` matches any number
    - `[a-zA-Z]` matches any letter, regardless of case

In this regex:

- `[a-zA-Z0-9.\_%+-]` Matches any number, `.` , `_`, `%`, `+`, `-`
- `[a-zA-Z0-9.-]` matches any letter (UPPER or lower case), number, `.`, `-`

### The OR Operator

The OR Operator is the `|` symbol which allows for "if not this, then that" situations.

In this regex:

N/A

### Flags

Flags will change how the entire function behaves.

- Case-insensitive matching: Javascript uses `i` (/hello/i matches "hello", "HELLO" or "HeLO", etc)

-Global Matching: Allows the regex to find all matches in the input instead of the first instance. Javascript uses `g`. (/hello/g finds all instances of "hello")

In this regex:

N/A

### Character Escapes

Character Escapes allows the matching of special characters.

In this regex:

- `\.` matches the actual `.` character
- `\@` matches the actual `@` character

## Author

I am FullStack Web Design Bootcamp student that is headed towards a career in web development. I have a wonderful family and great support. completing this course will help further my career goals.

Github Profile: https://github.com/dannadlerp/
