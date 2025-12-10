# week 6

## Error Searching

Read the whole error message.

Go to the line that the error points to.

Generall the first line is sufficient to search for online (i.e., search just the "message" not the "trace").

Message might be "top-down" or "bottom-up".

### NameError

Variables and functions names cast/assigned/combined incorrectly.

### TypeError

Trying to combined two different data types.

i.e., 1 + "1"

Trying to complete an equation with a string.

i.e., "1" + "1"

### ValueError

Value in a variable expected to be one type of data but is another.

e.g., trying to assign an integer instead of a string to a list of alpha characters.

### SyntaxError

Punctuation or formatting is incorrect.

### IndexError

The code tries to access a value that is out of bounds or not present.

i.e., in a 0-indexed array that contains 4 values, you try to call on the fourth value with [4] instead of [3]