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

But this code assigns `x` to total, and then evaluates `y`, doing nothing with it:
```ruby
total = x       # This is a complete expression
    + y         # A useless but complete expression
```

## Ruby Datatypes

### Numbers
![The Numeric class hierarchy in Ruby](/images/numeric_class_hierarchy.png)

![](https://github.com/vaibhav101/my-ruby-crash-course/raw/master/images/numeric_class_hierarchy.png)
Ruby includes five built-in classes for representing numbers, and the standard library includes three more numeric classes that are sometimes useful.

- All number objects in Ruby are instances of `Numeric`. All integers are instances of `Integer`.
- If an integer value fits within 31 bits (on most implementations), it is an instance of `Fixnum`. Otherwise, it is a `Bignum`.
- `Bignum` objects represent integers of arbitrary size, and if the result of an operation on `Fixnum` operands is too big to fit in a `Fixnum`, that result is transparently converted to a `Bignum`. Similarly, if the result of an operation on `Bignum` objects falls within the range of `Fixnum`, then the result is a `Fixnum`.
- **All `Numeric` objects are immutable; there are no methods that allow you to change the value held by the object. If you pass a reference to a numeric object to a method, you need not worry that the method will modify the object.**

### Strings

#### String Literals

##### Single Quoted String Literals
- These are the simplest form of string literals
- The only escape sequesces allowed are backslashes `'\\'` and single quotes `\'`
- No string interpolation is allowed (described later)


