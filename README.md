# My Ruby Crash Course
###### By Vaibhav Paliwal

## Features of the Ruby Language
Ruby is a **dynamic, interpreted, reflective, object-oriented**, general-purpose programming language

 - **Dynamic:** 
 - **Interpreted:**
 - **Reflective:**
 - **Object Oriented:**

## Ruby Lexical Structure

### Comments
- Comments in Ruby begin with a # character and continue to the end of the line
- Multiline comments are usually written simply by beginning each line with a separate # character
- Ruby has no equivalent of the C-style `/*...*/` comment
- There is no way to embed a comment in the middle of a line of code.

### Newlines as statement terminators
- In languages like C and Java, every statement must be terminated with a semicolon. 
- In the case of Ruby, if the Ruby code on a line is a syntactically complete statement, Ruby uses the newline as the statement terminator. If the statement is not complete, then Ruby continues parsing the statement on the next line.
- You can use semicolons to terminate statements in Ruby, too, but this is only required if you put more than one statement on the same line.

Some care must be taken due to this behaviour. For example the following code adds `x` and `y` and assigns the sum to `total`:
```ruby
total = x +     # Incomplete expression, parsing continues
    y
```

But this code assigns x to total, and then evaluates y, doing nothing with it:
```ruby
total = x       # This is a complete expression
    + y         # A useless but complete expression
```

## Ruby Datatypes

### Numbers
![The Numeric class hierarchy in Ruby](/images/numeric_class_hierarchy.png)
Ruby includes five built-in classes for representing numbers, and the standard library includes three more numeric classes that are sometimes useful.
