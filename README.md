# Regex Tutorial Starter Code
What Is a Regex?
A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

For example, the following regular expression can be used to verify that user input is a valid email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the @ symbol, followed by a domain.

Before you get started, watch this introduction to regular expressions videoLinks to an external site. and read Regex Tutorial: Matching a UsernameLinks to an external site. to learn how to identify the different components that make up a regex. If you need any additional help, there are many resources on the web. Feel free to do your own research to find one that can help you complete this assignment.

Once you have a better understanding of what these different parts of a regular expression do, you’ll need to explain what they do for a specific regex.

You can choose one of the following regular expressions or you can choose one that you found on your own (with the exception of the one that is covered in the Regex Tutorial: Matching a UsernameLinks to an external site.:

Matching a Hex Value – /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Matching a URL – /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

Matching an HTML Tag – /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

Summary
## Anchors
The anchors used in this regex expression for matching an email are ^ , which indicates the beginning of the string and $ to indicate the ending of the string. (m) , or multiline is not enabled, so the regex will end at $. Anchors in regular expressions are special characters or constructs that define specific positions within the input text where a match must occur. They do not represent actual characters, but rather positions relative to characters in the input string. Anchors are used to ensure that a certain part of the pattern is located at a specific position in the text. There are two main types of anchors:

## Quantifiers
Quantifiers define how many times a specific character or group should occur. For instance, + indicates that the preceding element should occur one or more times.A Quantifier specifies how many instances of the previous element (which can be a character, a group, or a character class) must be present in the input string for a match to occur. They also determine whether a regex will attempt a Greedy match or a Lazy match.They control the repetition of the preceding pattern.

## Bracket Expressions
Bracket expressions, denoted by [ ], define a character set from which a single character should match. For example, [a-z0-9_.-] matches lowercase letters, digits, underscores, dots, and hyphens.

Bracket expression show what set of of characters need to be matched. [a-z0-9_.-] a-z A single character between a and z that is case sensitive. 0-9 A single character between 0-9. _ Indicates that it must match the character and is case sensitive. . Must match the character and is case sensitive. - The character must match and is case sensitive.

[\da-z.-] \d Indicates the character matches a digit the same as [0-9]. a-z A single character between a and z that is case sensitive. . Must match the character and is case sensitive. - The character must match and is case sensitive.

[a-z.] a-z A single character between a and z that is case sensitive. . Must match the character and is case sensitive.

## Greedy-and-lazy-match
the terms "greedy" and "lazy" are more commonly associated with quantifiers like * (greedy) and *? (lazy), which control the repetition of preceding elements

## Boundaries
Instead of anchoring the regex match to the start and end of the subject, you have to specify that the start of the local part and the top-level domain cannot be part of longer words. This is easily done with a pair of word boundaries. Replace both ‹ ^ › and ‹ $ › with ‹ \b ›. For instance, ‹ ^[A-Z0-9+_.

## Back-references
We can use backreferences in a regular expression to ensure that the same value appears multiple times in a pattern. In the context of an email address, you might want to ensure that the domain name's last part (the top-level domain) matches the first part (the domain name) by using a backreference. \b[A-Za-z0-9._%+-]+@([A-Za-z0-9.-]+).\1\b

In this regex: \b[A-Za-z0-9._%+-]+@: Matches the username and "@" symbol. ([A-Za-z0-9.-]+): This is a capturing group that matches the domain name. The capturing group ( ) allows you to refer back to this matched value using a backreference \1. .\1: Matches a period (.) followed by the same value that was captured in the first capturing group. This ensures that the TLD matches the domain name. \b: Word boundaries to ensure the email address is matched as a whole word.

## look-ahead-and-look-behind
We can use lookaheads and lookbehinds in a regular expression to add more sophisticated matching conditions without actually consuming characters. Here's how you could modify the regex to include a positive lookahead to ensure that the TLD is the same as the domain name: \b[A-Za-z0-9._%+-]+@([A-Za-z0-9.-]+).(?=\1)[A-Za-z]{2,}\b

In this regex:

Challenge this week is to create a tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.

## Table of Contents
- [User-Story](#user-story)
- [Acceptance-Criteria](#acceptance-criteria)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contributing](#contributing)
- [Test](#test)


# User Story

AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines




# Acceptance Criteria

GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile

## Installation
There is no installation needed. Simply head on over to the deployed app on heroku using the link below.


## Usage
This app is ment for your to take notes on the fly, and once you are done with your task, you can simply and quickly delete it.

## License
This app is covered under MIT license. For details and limitations of this license please visit:
[License Link for MIT](https://opensource.org/licenses/MIT)

## Contributing
If you would like to share your feedback and/or contribute your best practices to make our code better, feel free to get in touch with us via:
  GitHub: [11-Note-Taker-ExpressJS - link]([https://github.com/VithusanU/NoteTaker](https://github.com/VithusanU/Regex_Tutorial)<br>

## Test
We are using jest for testing the development of the functions. No test have been written for this application yet.
<br>

### Deployed Links

1. You can find the URL of my GitHub repository that contains this code **here:** <br>[GitHub Repo - link](https://github.com/VithusanU/Regex_Tutorial)


# Credits

Github: VithusanU
Email: vithusan.business@gmail.com
 
