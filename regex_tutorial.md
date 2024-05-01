# Creating Complex Password Patterns Using Regex
In this guide, you will delve into creating a regex pattern for passwords. Each component of the expression will be explained, enabling readers to customize it according to their specific requirements.

### At a Glance
This regex pattern is designed for creating passwords that include one uppercase letter, one lowercase letter, one number, one special character, and are at least 8 characters in length. Developers can use this regex code to enforce complex password rules for user authentication.

### Contents
1. [Quantifiers](#quantifiers)
2. [Character Sets](#character-sets)
3. [Grouping and Capture](#grouping-and-capture)
4. [Bracket Expressions](#bracket-expressions)
5. [Lookahead](#lookahead)
6. [About the Author](#about-the-author)

## Key Components of the Regex Pattern

### Quantifiers:
Two main quantifiers are utilized in this regex pattern: * and {8,}. The * signifies zero or more occurrences of the preceding token. In this regex, * is applied before each character set, allowing flexibility in accepting various character types. Another quantifier, {8,}, sets the minimum password length to 8 characters. This can be adjusted based on specific requirements; for instance, {12,} for a 12-character minimum.

### Character Sets:
This regex requires four types of characters: uppercase letters, lowercase letters, numbers, and special characters. Uppercase letters are represented as [A-Z], lowercase letters as [a-z], numbers as [0-9], and special characters as [\!@#$%^&*()\\[\]{}\-_+=~\|:;"'<>,./?]. The set of special characters can be customized by adding or removing characters within the square brackets, enabling tailored password rules.

### Grouping and Capture:
Capturing groups are implemented to group multiple tokens for extracting substrings or backreferences. Each capturing group in this regex captures specific requirements of the password:

* At least one number: (.*[0-9])
* At least one uppercase letter: (.*[A-Z])
* At least one lowercase letter: (.*[a-z])
* At least one special character: (.*[\!@#$%^&*()\\[\]{}\-_+=~\|:;"'<>,./?])
* The rest of the password: (.*)

### Bracket Expressions:
Bracket expressions, denoted by [...], match any single character within the enclosed list. They can also include range expressions separated by a hyphen. The regex implements bracket expressions to define allowed special characters, uppercase letters, lowercase letters, and numbers. Range expressions are indicated with a hyphen, e.g., [A-Z], [a-z], [0-9].

### Lookahead:
Multiple positive lookahead segments are utilized to ensure the presence of at least one uppercase letter, one lowercase letter, one number, one special character, and a minimum length of 8 characters. Positive lookahead is implemented by (?= ). In this regex, positive lookahead is used with capturing groups for each password requirement:

* Number lookahead: (?=(.*[0-9]))
* Uppercase letter lookahead: (?=.*[A-Z])
* Lowercase letter lookahead: (?=(.*[a-z]))
* Special character lookahead: (?=(.*[\!@#$%^&*()\\[\]{}\-_+=~\|:;"'<>,./?]))
* General character lookahead: (?=(.*)), allowing any character besides line breaks.

### About the Author
I am Pedro M. Gonzalez, currently a student at the Northwestern University Web Development Coding Bootcamp. Expected graduation date is June 2024. You can explore more of my work on [GitHub](https://github.com/orion888888).