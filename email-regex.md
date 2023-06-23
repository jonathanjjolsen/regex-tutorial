# Email Regex Tutorial

Most people living in the 21st century have an email. Its almost impossible to be in today's workforce without one. Aside from the obvious ability to send and recieve messages, the email address is also commonly used as a username log in for other websites. Lets use Amazon as an example. When you create an account with Amazon, one of the first things they require from you is your email. This allows Amazon to send you emails about sales and order updates. "But what if I enter my email incorrectly?" Luckily, in order to mitagate this from happening as often, many log in pages use something called a "Regular Expression" or "Regex." The pupose of a regex is to identify patterns within a string. This allows the backend javascript to validate that the user has entered their email correctly. This is just one of the many uses for a regular expression but in order to find out more about the email validation regex, continue reading through this document.

## Summary

As mentioned above, this document is going to outline the use and functionality of an email validation regular expression. These are crafted in order to verify that a user has entered the correct format of the email. It checks for things such as an "@" symbol or a "." near the end. The different sections of this document will disect the different components that go into the creation of a regex and how they all function. Below is an example of a basic email validation regex that we will be using throughout the rest of this tutorial.<br/>
<br/>
`/^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors are utilized to signify the beginning and end of where the validation should occur within the entered information.<br/> <br/> `/^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})$/`<br/> 
<br/> In the above example, we can see that there are two anchors held within the code. The first is the `^` symbol. This is called a caret and identifies that the regex should start checking for validity at the beginning of the entered info. The second symbol used is the `$`. Using a dollar sign lets the script know that we want it to check at the end of the entered information. When taking viewing expression as a whole, we can identify that the caret is used at the beginning and the dollar sign is used at the end. This means that the entered email will be validated from beginning to end.

### Bracket Expressions
Bracket expressions are the meat of the regular expression. They identify what characters are okay to be used, and which are not by using character classes. Held within each of the different sections of brackets in the original regex are the classes which are allowed to be included. Lets take a closer look at one of the examples we have.<br/>
<br/>`[a-zA-Z0-9._%-]`<br/>
<br/>When this is broken down even futher it becomes very clear what characters are to be used for validation: Lowercase Letters `a-z`, Uppercase Letters `A-Z`, Numbers `0-9`, and a list of chosen symbols `._%-`. As long as the characters entered fall into one of these categories, the email will be accepted as valid.

### Quantifiers
Quantifiers are used to ensure that one or more of the patterns listed before it are satisfied. The first example of this is the use of the `+` sign. `([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+` Uppon closer inspection we can identify that the requirement is at least one lowercase, uppercase, number, or predetermined symbol before and after the `@` in order to be considered valid. If we use the example, `john.doe@gmail.com` the quantifier would be satisfied because there is at least one of the aformentioned characters used before and after the `@` symbol. The second use of a quatifier in this example comes toward the end of the expression in the form of `{2,6}`. This piece of the regex sets a minimum and maximum number of times for the pattern to be repeated. If we reuse the fake email from earlier, it is clear that the email would pass this inspection. `.com` would fall between the parameters being that it is exactly 3 characters long following the `.`.

### Grouping Constructs
Grouping constructs are used to form collections of patterns. They are signified by the use of `( ... )`. In many cases they are used to form smaller groups within a larger regex. In our case the entire expression is grouped together. Take a close look at where the parentheses are located.<br/>
<br/>`/^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})$/`<br/>
<br/>They are at the beginning of the first pattern and the end of the last pattern. This aids in establishing the entire email as one. The reason we want this to all be as one is to validate that each section of the entered email meets the criteria of the regex. This will ensure correct formatting across the board from the "john.doe" to the ".com" at the end.

### Character Classes
The previously mentioned character classes play a crucial role in the operation of a regex. We've already established that they are held within the `[ ... ]` operators and help identify which characters are allowed to be used. Lets go over them again.<br/>

<br/>`a-z`: Lowercase Letters
<br/>`A-Z`: Uppercase Letters
<br/>`0-9`: Numbers
<br/>`._%-`: Additional Characters

### Character Escapes
A character escape is called using backslash when the regex should interperet the following symbol as a literal character rather than its specialized operation. This might be a little tricky to understand so lets dive deeper into the example.<br/>
<br/>`/^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})$/`<br/>

Because we have a `\` in front of the `.`, it is calling for a literal period to be in that position. This is the "." in ".com". If the `\` was not there, the default special use for a period is any character except for a newline.

## Author
### Jonathan Olsen
This tutorial was a prompt for a school assingment. If you have any questions, you can reach me directly at: <br/>
<br/>jonathanjolsen@gmail.com<br/>
<br/>Or message me directly on github.<br/>
<br/>GitHub: https://github.com/jonathanjjolsen
