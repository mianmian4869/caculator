# code specification
## Indentation
- The number of characters per line cannot exceed 120. When the number of characters in a line exceeds 120, you can wrap the line
- Line feed Line indentation is controlled according to the following constraints: function argument line feed. The first letter of the first argument after a line feed should be left aligned with the first letter of the function's first argument
- If the expression contains the "()" operator, there should be no line wrap
```
//bad
longName1 = longName2 * (longName3 + longName4
longName5) + 4 * longname6;
//good
longName1 = longName2 * (longName3 + longName4 - longName5)
+ 4 * longname6;
```
## Variable naming
- An identifier cannot start with a number, but it can contain a number.
- Identifiers can contain only letters, numbers, underscores, and dollar signs.
- Identifiers cannot be JavaScript keywords or reserved words
##  Maximum number of characters per line
- The number of characters per line cannot exceed 120.
##  Maximum number of function lines
- The number of characters per line cannot exceed 100.
##  Function and class naming
- Function names must start with a letter, underscore, or $sign, and cannot start with a number.
- Function names cannot contain Spaces, punctuation marks, or special characters, such as @, #, and %.
- The function name can contain letters, numbers, underscores, or $signs, but cannot end in a number.
- The function name should be descriptive, able to clearly express the function's role and function.
- Function names should use the hump naming method, that is, the first word is lowercase and the following word is uppercase, such as getUserName
## Constant
- Constant refers to the data that remains unchanged during the running of the program;
  - "345" is a numeric constant, "JavaScript" is a string constant, true or false is a Boolean variable, etc.
## Blank line rule
- After a variable is declared (no blank line is required when the variable is declared on the last line of the code block)
- Before a comment (no blank line is required when the comment is on the first line of the code block)
- After a code block (no blank line is required in function calls, arrays, or objects)
- At the end of the file
## Annotation rules
- Use /***/ for multi-line comments
- Use // for single-line comments
## Space before and after operator
- Use Spaces to separate operators.
```
 // bad
const x=y+5;
// good
const x = y + 5;
```
## Code block
- All multi-line code blocks must be wrapped with braces after the if.
```
// bad
if (name)
	return;
// good
if (name) {
	return;
}
```
