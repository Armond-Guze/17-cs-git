# REGEX Tutorial

Regex are regular expressions or collections of characters that produce text serach patterns. Used mostly in word processors, text editors, and search engines. You can find descriptions of a specific regex, that looks like a hexadecimal in this README. A letter and a whole number value system is used for hexadecimals.

## Summary

The REGEX found in this intinerary will be explaining a matching email expression. We will deconstruct this following statement : /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.

Ensure that user creates an email address that starts with an arbitrary amount of characters before the @ symbol, followed by a domain, each element of this regex has a specific duty.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Just Checking In](#just-checking-in)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex-Components

### Anchors


The regular expression employed for email matching incorporates specific anchors: '^' denotes the start of the string. Its crucial to note that the multiline flag '(m)' isn't activated, meaning the regex interpretation concludes upon encountering '$'. In essence, these anchors delineate the exact boundaries within which the regex engine operates, ensuring precise email identification within the text.

### Quantifiers

A quantifier defines the quantity of occurrences required for the preceding element, which could be a character, a group, or a character class, to constitute a match within the input string. In simpler terms, it dictates the number of times a specific element must appear for the regex pattern to successfully match against the text being evaluated.

In an email address, various components like the local part (before the '@' symbol) and the domain part (after the '@' symbol) have different requirements regarding the number of characters they can contain.

### OR Operator

OR operators can be useful when defining patterns that accommodate variations in email formats. Email addresses can have many structures, and regex patterns must be flexible enough to handle these variations.

### Character Classes

There are several Character Classes you need to understand when trying to match emails using REGEX, We'll start with Bracket Expression!

Bracket expressions are denoted by square brackets [], are used to specify a set of characters that the regex engine should match. They allow you to define custom character classes that can match any character within the set.

Those character classes include

1. Alphanumeric Characters: [A-Za-z0-9]
2. Special Characters: ['.','%', '+''.', '_', '%', '+', and '-']
3. Domain Characters: [A-Za-z0-9.-]

### Grouping and Capturing

By using grouping and capturing effectively in your regex pattern, you can not only match emails but also extract and manipulate specific components of the email addresses as needed.

Grouping, denoted by parentheses (), allows you to define subpatterns within your regex. This is very useful for specifying sections of the pattern that should be treated as a single unit.

Capturing, also facilitated by grouping, is the process of extracting the text matched by a specific group in the regex pattern. When a regex match occurs, each group captures the portion of the matched text that corresponds to its subpattern. This allows you to retrieve and work with specific parts of the matched text.

## Just Checking In

Are you still with me? I know it can be alot to take in but trust me it's all worth it!

## Bracket Expressions

Bracket expressions, also known as character classes, are a fundamental component of regular expressions used for pattern matching. They allow you to specify a set of characters that the regex engine should match. For example, [abc] would match any single character that is either 'a', 'b', or 'c'. These expressions are enclosed within square brackets [], and they provide a convenient way to define custom sets of characters that fulfill specific matching criteria.

## Greedy and Lazy Match

Greedy and lazy matching can be important considerations depending on the structure of the email addresses you are trying to match. Greedy matching may lead to overmatching if not used carefully, while lazy matching can help ensure more precise matches by stopping at the earliest opportunity.

## Boundaries

By using boundaries in your regex pattern, you can ensure that the pattern matches email addresses within the desired context, such as when they appear at the beginning or end of a line.

The caret symbol (^) asserts the start of the line or string. When placed at the beginning of a regex pattern, it ensures that the pattern only matches if it starts at the beginning of the input text.

## Back-references

Back references are helpful for ensuring consistency and validation within complex regex patterns, including those used for matching emails.

## Look-ahead and Look-behind

These are assertions that provide a powerful way to add additional conditions or constraints to regex patterns when matching emails, allowing for more precise and flexible matching based on specific requirements or criteria.

Look-ahead assertions, denoted by (?=...), specify a condition that must be met after the current position in the string for the match to succeed.
