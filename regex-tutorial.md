# RegEx 101: Pattern Matching and Grouping

String manipulation can be a difficult task but with regular expressions it can become much easier. By learning how to use regular expressions programmers can unlock new avenues to solve problems and create new solutions.

## Summary

Regular expressions are a way to match strings using a set of character combinations. Regular expressions can be created in two different ways, by creating the expression literal or by calling the contstructor. By creating our own regular expressions working with strings can become mush less of a hassle and can shorten our code greatly. In this tutorial we will learn just how to do that.

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
The components that are used to build a regular expression include:
* Single Characters: These are characters with no special signigicance and are used to match characters in the target string.

* Wild Card: The . character mathces any single character.

* Bracket Expressions: A bracket expression represents a character set via a list of characters enclosed by the square brackets. Within the brackets we specfiy what characters we are trying to match. Further we can add the ^ character which mean NOT. Within the brackets we typically add escape characters that are discussed later. Bracket expressions are the foundation of patter matching using regex.

### Anchors
Anchors can be used to match the position of a target string rather than the characters in it. For example applying ^a to "abc" matches a, while $c mathces c.



### Quantifiers
Regular expressions use quantifiers to match for a certain amount of times a character appears in a string.

These include:
* (*): Matches when no occurences of the specefied charater are present.

* (+): Matches when 1 or more occurences are in the target string.

* (?): Matches when 0 or 1 occurences are present in the string.

* ({n}): Matches when the exact amount of characters are in the string.

* ({m, n}): Matches when characters are between the given values.

### Grouping Constructs
Grouping constructs can be used to capture the substrings of an input string. And can be used to do the following:
* Match subexpressions that is repeated in the input string.

* Apply quantifiers.

* Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

### Bracket Expressions
Bracket expressions tell us when a character class or quatifier statment begins. 
For example:
/?([a-g0-3])$/


### Character Classes
Character classes can be used to match specefic characters in the target string. A simple example includes [a-z] which matches any lower case letters, on the other hand we have [0-9] which matches any number. We can then combine these to match more specefic values such as [i-k5-7]. Character classes are simple but provide a lot of use cases.

### The OR Operator
The OR operator in a regular expression is similar to the one found in JS. We can match for two different patterns and will return the one that can be applied.

The OR operator is | and here is an example:
([a-c0-9]{1}|[a-c0-9])

### Flags
Flags add more options such as global searching and case insensitive searching. These flags can be used seperately or together in any order.

Some examples include:
* g - Global search.

* i - Case insensitive search

* m - Multi line search.

* d - Return indices for substring matches.

Using these flags adds a new dimension to the already powerful features of reguler expressions.

### Character Escapes
In this section we will cover the different escape characters that can be used to create a regular expression.

\d - Mathces any digit (0-9)

\D - Matches any digit that is NOT a number

\w - Matches all characters in a string

\W - Matches any character that is NOT a number or letter

\s - Matches a single white space in a string, this can help us split sentences

\S - Matches a singel character other than a white space

\t - Matches a tab

\r - Matches a carriage return

\n - Matches a line feed

## Author

Carlos Hernandez, is a CS graduate seeking new opputunites in the world of web dev.

GitHub: https://github.com/confusion-matrix