# Email Regex Tutorial

Most people living in the 21st century have an email. Its almost impossible to be in today's workforce without one. Aside from the obvious ability to send and recieve messages, the email address is also commonly used as a username log in for other websites. Lets use Amazon as an example. When you create an account with Amazon, one of the first things they require from you is your email. This allows Amazon to send you emails about sales and order updates. "But what if I enter my email incorrectly?" Luckily, in order to mitagate this from happening as often, many log in pages use something called a "Regular Expression" or "Regex." The pupose of a regex is to identify patterns within a string. This allows the backend javascript to validate that the user has entered their email correctly. This is just one of the many uses for a regular expression but in order to find out more about the email validation regex, continue reading through this document.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.<br/>
<br/>
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
Anchors are utilized to signify the beginning and end of where the validation should occur within the entered information. In this example: `/^([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,6})$/` we can see that there are two anchors held within. The first is the `^` symbol. This is called a caret and identifies that the regex should start checking for validity at the beginning of the entered info. The second symbol used is the `$`. Using a dollar sign lets the script know that we want it to check at the end of the entered information. When taking a closer look at the expression, one should identify that the caret is used at the beginning and the dollar sign is used at the end. This means that all of the entered email is going to be validated.

### Bracket Expressions

### Quantifiers
Quantifiers are used to ensure that one or more of the patterns listed before it are satisfied. The first example of this is the use of the `+` sign. `([a-zA-Z0-9._%-]+@[a-zA-Z0-9.-]+` Uppon closer inspection we can identify that the requirement is at least one lowercase, uppercase, number, or predetermined symbol before and after the `@` in order to be considered valid. If we use the example, `john.doe@gmail.com` the quantifier would be satisfied because there is at least one of the aformentioned characters used before and after the `@` symbol. The second use of a quatifier in this example comes toward the end of the expression in the form of `{2,6}`. This piece of the regex sets a minimum and maximum number of times for the pattern to be repeated. If we reuse the fake email from earlier, it is clear that the email would pass this inspection. `.com` would fall between the parameters being that it is exactly 3 characters long following the `.`.

### Grouping Constructs


### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
