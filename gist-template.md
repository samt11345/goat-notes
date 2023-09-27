# Title RegEx

Hello! and thank you for taking time to learn with me so the video I found on youtube about Regex and how to use it specificly matching an email.
## Summary

so i will be explaining thow to use regex to match an email adress so Using regular expressions (regex) to match an email address involves creating a pattern that fits the common structure of email addresses. An email address typically includes a local part (username) followed by the "@" symbol and a domain name. here is an example of what a complete string will look ^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$


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
so to start with understanding regex we have to start small and go from there so the way i will explain everything will be gradually increasing in difficulty but i will do my best to keep it as simple as i can. 


1-Regular Expressions start within foward slashes /  / anything in the foward slashes will be your regular expression. also at the end of the expression you need to give it a flag for example /./g the g at the end is the flag which is letting the expression know that it is a global flag and can search the entire string of code.

2-Literals which means exactly how it sounds it takes in characters that match themselves for example 'a','1','#' in this example we are using literals so we are literally looking for the letter a, the number 1, and the # symbol.

2-Metacharacters these are characters that already have a pre-defined meaning example

 -($) matches the end of a string .
 -(^): Matches the start of a string.
 -(|): Functions as an OR operator.
 -(?): Matches zero or one occurrence of the preceding element.
 -(+): Matches one or more occurrences of the preceding element.
 -(*): Matches zero or more occurrences of the preceding element. 
 -(.): Matches any character except a newline.




^: Asserts the start of the string.
[a-zA-Z0-9._-]+: Matches the local part.
@: Matches the "@" symbol.
[a-zA-Z0-9.-]+: Matches the domain name (excluding the top-level domain).
\.: Matches a dot before the top-level domain.
[a-zA-Z]{2,}: Matches the top-level domain with at least two alphabetical characters.
$: Asserts the end of the string.

### Anchors

^ - Matches the start of a string.
$ - Matches the end of a string.
so you in most situations would need both of these so you can match the whole string becuase ^ does match the start and the $ matches the end so everything works.
### Quantifiers
A bracket expression in regex, often denoted by square brackets [], is a way to specify a set of characters you want to match in a certain position in your pattern.

### Grouping Constructs
grouping contructs allows you to organize and manipulate parts of a pattern as a unit.

() parentheses define a group and anything that is inside of them is treated as a unit,they also allow you to capture the matched content you can refrence it as captured content.

here is an example with capturing '(\d{3})-(\d{2})'
so what is happening here is the first half of the code before the hyphen is looking for 3 digits which would be in the first group becuase of the (\d{3}) which is looking for 3 and on the other side with the remaining code after the hyphen it is looking for 2 digits.

### Bracket Expressions
to start bracket expressions you will start with [] this is how you can specify a set of characters that you want to match in a specific position in your pattern 

for example if i were to do [aeiou] matches any vowel (a, e, i, o, or u). that is exactly would it would try to find, you can also find a range like [a-c] which will only find lower case a,b or c.

you may also combine ranges like [a-zA-Z] which is looking for any letter regular or capitol and you can also add [0-9] which will get you any number in that range, which is also another thing that can be combined which would look something like this [a-zA-Z0-9]

### Character Classes
[abc] - Matches any character within the brackets (a, b, or c).
[^abc] - Matches any character not in the brackets (not a, b, or c).
[a-z] - Matches any lowercase letter.
so with these you can search for specifics for example [a-z] this will search any letter from a-z but as you can see we inserted the lower case a-z, which means we are only searching for the lower case letters so in order for us to search for capitol letters we would just have to do this [A-Z] or we can search for both by using [a-zA-Z]  using this will get us all letters lowercase and capital.
### The OR Operator
The "or" operator in regular expressions is represented by the vertical bar |. It allows you to match either one pattern or another.giving more flexibility and opening up more options and routes! 

Here's a simple explanation: The | operator is used to define alternatives. It's like saying "match this pattern OR that pattern."

so if you were to use the "or" operator it would look something like this hamburger|hotdog 


### Flags
In regex, flags are special instructions that modify how the pattern is matched. They can change things like case sensitivity, the way special characters are interpreted, and how the pattern spans multiple lines.
### Character Escapes
\d - Matches any digit (0-9).
\w - Matches any word character (alphanumeric and underscore).
\s - Matches any whitespace character.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
