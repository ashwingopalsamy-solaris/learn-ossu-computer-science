# [Intro CS](https://cs.ossu.dev/coursepages/intro-programming/)

Although I am introduced to programming, fundamentals of computer science, giving a skim through [intro-cs](https://cs.ossu.dev/coursepages/intro-programming/) won't hurt and I'm confident that there'll still be unknowns in the absolute basics.

## Introduction to Programming with Python

### Functions
* Reusable blocks of code that perform specific tasks.
* Defined using the `def` keyword followed by the function name and parentheses.
* Can optionally accept inputs (arguments) and produce outputs (return values).

```python
def greet(name):
  print("Hello, world!")
  print("I'm", name, sep=' ')

greet("Ashwin")
```

### Variables
* Named containers that store data.
* Used to hold values that can change during program execution
```python
name = 'James Clear'
age = 38
print("Atomic Habits is written by", name, "who is now", age, "years old", sep=' ')
```

### Parameters
* Placeholders within the function definition that represents the arguments that needs to be passed.

### Return Values
* Optional outputs that are produced by a function
* Specified using the `return` keyword within the function
* Used to send the data back to the part of the code that was called by the function.

### Input Function:
* In `py`, the `input` function treats the input values as `strings`, even if the user enters the numbers.
* We can either define during the input on which data type we would prefer.
* ```python
  age = int(input("Age: "))
  ```
* or
* ```python
  age = input("Age: ")
  print(int(age))
  ```
* or using `f-strings`:
* ```python
  x = input("Age: ")
  print(f"Age: ", {int(age)})
  ```


### Escaping Characters
* A way to include, perform certain tasks within strings that would otherwise be interpreted by the programming language in a particular way.
* Done by using backslash (`\`) before the special character.

### Common Escaped Characters
* `\"` - Double Quote.
* `\'` - Single Quote.
* `\n` - New Line
* `\t` - Horizontal Tab

### Strings & Parameters
```python
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```
* A String Datatype in Python is defined with `str`.
* A `sep` argument in the `print` function acts as a separater between each statement inside the print statement. By default, a `sep` argument will have the single space ` `.
* By default, an `end` argument at the end of `print` function will create a new line after this function is run.
* We can tweak it to not create a new line by adding a `end=""` at the end of `print` function.
* "F-Strings" are a way to embed variables directly within a string.

```python
name = input("What's your name? ")
print(f"Hello, {name}")

age = input("Age: ")
print(f"Age: {age}")
```

#### String Manipulations
- `s.upper()` - Converts all characters in a string to uppercase.
- `s.lower()` - Converts all characters in a string to lowercase.
- `s.title()` - Converts all characters in a string to title case.
- `s.strip()` - Removes leading and trailing whitespaces (spaces, tabs, newlines) from a string.
- `s.find(sub)` - Returns the index of the first occurance of the substring within a string or `-1` if unfound.
- `s.replace(old, new)` - Returns a new string where all occurances of `old` are replaced with `new` in `s`.

#### String Traversal & Slicing:
- `s[i]`: Accesses a character at a specific index `i` (O-based indexing)
- `s[i:j]`: Extracts a substring from index `i` (inclusive) to `j` (exclusive).
- `s[::-1]`: Reverses the string. (Useful for palindrome checks).

#### Advanced String Methods:
- `s.split(sep)`: Splits `s` ito a list of substrings based on the delimiter `sep`.
- `join(list)` : Joins elements from a list or iterables, into a string using a separater.
- `s.isalnum()`: Checks if the string is an alpha-numeric.
- `s.isdigit()`: Checks if all characters in `s` are digits.
- `s.isalpha()`: Checks if all characeters in `s` are alphabetic.
- `s.startswith(prefix)`: Checks if a string starts with given `prefix` substring.
- `s.endswith(suffix)`: Checks if a string ends with the given `suffix` substring.

### Regular Expressions:

* A powerful tool for searching, matching and mainpulating text based on patterns.
* In Python library, we have `re` module for performing regular expressions.

#### Common Regex Metacharacters:

- `.` (dot): Matches any single character (except newline by default).
- `\w` (word character): Matches letters, numbers, and underscores.
- `\d` (digit): Matches any decimal digit (0-9).
- `\s` (whitespace): Matches any whitespace character (space, tab, newline).
- `^` (caret): Matches the beginning of the string.
- `$` (dollar sign): Matches the end of the string (or before the newline at the end).
- `[]` (character set): Matches any character within the brackets (e.g., [aeiou] matches any vowel).
- `-` (hyphen): Used within a character set to specify a range (e.g., [a-z] matches lowercase letters).
- `*` (asterisk): Matches the preceding character zero or more times.
- `+` (plus sign): Matches the preceding character one or more times.
- `?` (question mark): Matches the preceding character zero or one time (optional).
- ``| (pipe): Matches either the pattern before or the pattern after the pipe (OR operator).
- `()` (parentheses): Groups characters for complex patterns or capturing substrings.

#### Basic Regex Functions in re:

- `re.search(pattern, string)`: Searches for the first occurrence of the pattern in the string. Returns a match object if found, otherwise None.
- `re.match(pattern, string)`: Similar to search, but only matches if the pattern occurs at the beginning of the string.
- `re.findall(pattern, string)`: Finds all non-overlapping occurrences of the pattern in the string. Returns a list of matched substrings.
- `re.sub(pattern, repl, string)`: Substitutes all occurrences of the pattern in the string with the repl replacement string.