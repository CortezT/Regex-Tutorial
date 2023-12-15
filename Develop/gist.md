# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

In this tutorial, we'll be diving into the intricacies of regular expressions. We'll cover various components such as anchors, quantifiers, the OR operator, character classes, flags, grouping and capturing, bracket expressions, greedy and lazy matching, boundaries, back-references, and look-ahead and look-behind.

Let's start by looking at the regex pattern we'll be using as an example throughout this tutorial:
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

- Anchors, represented by ^ and $, assert specific positions in the input text. ^ asserts the start of a line, and $ asserts the end of a line. They ensure that the entire input matches the regex pattern from start to finish.

'^' // The caret symbol asserts the start of a line
'$' // The dollar sign asserts the end of a line

- Example
  - Input: john.doe@example.com
  - Explanation: The ^ anchor ensures that the match starts at the beginning of the string.

### Quantifiers

- Quantifiers specify the number of occurrences of the preceding element in the regex pattern. Common quantifiers include + (one or more occurrences), * (zero or more occurrences), ? (zero or one occurrence), {n} (exactly n occurrences), {n,} (n or more occurrences), and {n,m} (between n and m occurrences).

+ // Matches one or more occurrences
* // Matches zero or more occurrences
? // Matches zero or one occurrence
{n} // Matches exactly n occurrences
{n,} // Matches n or more occurrences
{n,m} // Matches between n and m occurrences

- Example:
  - Input: john.doe123@example.com
  - Explanation: The + quantifier allows one or more occurrences of alphanumeric characters before the @ symbol.

### OR Operator

- The OR operator, represented by |, allows for the alternation of patterns. It matches either the pattern on the left or the pattern on the right.

(a|b) // Matches either 'a' or 'b'

- Example:
  - Input: john.doe@example.com or jane_doe@example.com
  - Explanation: The | OR operator matches either a dot (.) or an underscore (_) within the username.

### Character Classes

- Character classes, enclosed in square brackets [], allow you to match any single character from a set. They are useful for specifying ranges of characters or creating negated character classes.

[aeiou] // Matches any vowel
[0-9] // Matches any digit
[a-zA-Z] // Matches any uppercase or lowercase letter

- Example:
  - Input: john.doe123@example.com
  - Explanation: The [a-zA-Z] character class matches any uppercase or lowercase letter in the domain.


### Flags

- Flags, such as /i, /g, and /m, modify the behavior of the regex pattern. They can make the matching process case-insensitive, enable global matching to find all matches, and facilitate multi-line matching.

/i // Case-insensitive matching
/g // Global matching (find all matches)
/m // Multi-line matching

- Example:
  - Input: john.doe@example.com
  - Explanation: No specific example for flags in this pattern, as flags are not explicitly used.

### Grouping and Capturing

- Parentheses () are used for grouping and capturing parts of the regex pattern. This is essential for extracting specific information from the matched text.

([a-z]+) // Captures one or more lowercase letters

- Example:
  - Input: john.doe@example.com
  - Explanation: The ([a-z]+) captures the username "john" as a group.

### Bracket Expressions

- Bracket expressions, also within square brackets [], match a single character from a specified set. However, they offer more flexibility than character classes, allowing you to include ranges and create negated expressions.

[a-z] // Matches any lowercase letter
[^0-9] // Matches any character that is not a digit

- Example:
  - Input: john.doe@example.com
  - Explanation: The [0-9] bracket expression matches any digit in the username.

### Greedy and Lazy Match

- Quantifiers are, by default, greedy, meaning they match as much as possible. Adding a ? after a quantifier makes it lazy, matching as little as possible.

.* // Greedy match (matches as much as possible)
.*? // Lazy match (matches as little as possible)

- Example:
  - Input: john.doe@example.com
  - Explanation: The .* greedy match matches the entire local part of the email address.

### Boundaries

- Boundaries, represented by \b, ensure that a match occurs at a specific position in the text, such as the start or end of a word.

\bword\b // Matches the word 'word' as a whole word

- Example:
  - Input: word@example.com
  - Explanation: The \b boundaries ensure that the match occurs at the start and end of the word "word."

### Back-references

- Back-references, represented by \1, allow you to refer back to a captured group within the regex pattern.

(\w)\1 // Matches repeated word characters

- Example:
  - Input: aa@example.com
  - Explanation: The (\w)\1 back-reference ensures that repeated word characters are matched, such as the "aa" in the username.

### Look-ahead and Look-behind

- Look-ahead and look-behind assertions, represented by (?=...), (?!...), (?<=...), and (?<!...), allow you to assert conditions before or after the current position without including them in the actual match.

(?=...) // Positive look-ahead
(?!...) // Negative look-ahead
(?<=...) // Positive look-behind
(?<!...) // Negative look-behind

- Example:
  - Input: john.doe@example.com
  - Explanation: The (?=...) look-ahead assertion could be used to check if a dot is followed by another character (e.g., (?=.)), ensuring it is not the last character in the local part.

## Author

This tutorial is brought to you by Trystan Cortez. Connect with me on GitHub @CortezT.


