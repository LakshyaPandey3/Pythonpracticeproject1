<h1>Pythonpracticeproject1</h1>
<hr>
<b>My Python Practice Project 1</b>
<hr>
📌 Project Description
<hr>
In this project, I learned how to convert a JSON file into a CSV file while understanding each line and every word of the code in detail.
<hr>

This project focuses on:

-> Reading JSON data from a file

-> Parsing JSON into Python objects

-> Converting structured data into CSV format

-> Writing the output to a CSV file

-> Handling errors properly using try-except

<hr>
<b><h1>🔎 Line-by-Line Deep Explanation</h1></b>
<hr>

> Line 1: import json:
<hr>
-> import – A Python keyword that tells the interpreter to load and make available an external module.

-> json – Stands for "JavaScript Object Notation." This is a built-in Python module that provides functions to work with JSON data (parsing JSON text into Python     objects and converting Python objects back to JSON text).

-> Purpose – This line makes available functions like json.loads() and json.dumps() that we use later in the code.
<hr>
> Line 3: if __name__ == '__main__':
<hr>
-> if – A conditional statement that checks whether the following condition is true.

-> name – A special Python variable that contains the name of the current module/script.

-> When you run a Python file directly, __name__ is set to the string '__main__'.

-> When you import a Python file as a module, __name__ is set to the module's name.

-> == – The equality operator; checks if the left side equals the right side.

-> 'main' – A string literal that represents the name given to the main script.

-> Purpose – This condition ensures the code below only runs when the script is executed directly, not when it's imported as a module in another script. This is a    Python best practice.
<hr>
> Line 4: try:
<hr>
-> try – A keyword that begins a "try-except" block used for error handling.

-> Purpose – The code inside the try block will be executed, and if any error occurs, it jumps to the except block instead of crashing.
<hr>
> Line 5: with open('input.json', 'r') as f:
<hr>
-> with – A context manager keyword that ensures proper resource management (automatically closes files).

-> open() – A built-in Python function that opens a file.

-> 'input.json' – A string literal specifying the filename to open.

-> 'r' – A mode string meaning "read" mode (read-only access to the file).

-> as – A keyword that assigns the opened file object to a variable.

-> f – A variable name (short for "file") that references the opened file object.

-> Purpose – This opens the file named input.json in read mode and assigns it to the variable f. The with statement ensures the file is automatically closed when     the block ends.
<hr>
> Line 6: data = json.loads(f.read())
<hr>
-> data – A variable that will store the parsed JSON data.

-> = – The assignment operator; assigns the right-side value to the left-side variable.

-> json.loads() – A function from the json module that takes a JSON-formatted string and converts it into a Python object (usually a list or dictionary).

-> loads stands for "load string."

-> f.read() – A method called on the file object f that reads the entire contents of the file as a string.

-> Purpose – This reads the entire JSON file as text, then converts it from JSON format into a Python data structure ( likely a list of dictionaries ).
<hr>
> Line 8: output = ','.join([*data[0]])
<hr>
-> output – A variable that will store the CSV output.

-> = – Assignment operator.

-> ',' – A comma string literal; this is the character used to join elements.

-> .join() – A string method that combines list elements into a single string, with the string it's called on as a separator.

-> *[data[0]] – A list creation using the unpacking operator.

-> * – The unpacking operator; expands a sequence into individual elements.

-> data – The parsed JSON data (a list of dictionaries).

-> data[0] – Access the first element (index 0) of the data list.

-> *[data[0]] – Creates a list from the keys of the first dictionary.

-> Purpose – This creates the header row of the CSV file by joining the dictionary keys (like "Name", "age", "birthyear") with commas.
<hr>
> Line 9: for obj in data:
<hr>
-> for – A loop keyword that iterates over a sequence.

-> obj – A variable name that will hold each item during iteration (short for "object").

-> in – A keyword meaning "from" or "within."

-> data – The list of dictionaries we parsed earlier.

-> Purpose – This loop goes through each dictionary in the data list one at a time, storing each one in the variable obj.
<hr>
> Line 10:
<hr>
-> output += f'\n{obj["Name"]},{obj["age"]},{obj["birthyear"]}'

-> output – The string variable we're building.

-> += – The augmented assignment operator; equivalent to output = output + ... (appends to the string).

-> f – Prefix indicating an f-string (formatted string literal) that allows embedding expressions inside {}.

-> '\n' – A newline character (starts a new line).

-> {obj["Name"]} – Embedding an expression; accesses the "Name" key from the obj dictionary and inserts its value into the string.

-> , – A comma character (CSV separator).

-> {obj["age"]} – Inserts the "age" value.

-> , – Another comma separator.

-> {obj["birthyear"]} – Inserts the "birthyear" value.

-> Purpose – This appends a new line to the CSV output, with data from the current object separated by commas.
<hr>
> Line 12: with open('output.csv', 'w') as f:
<hr>
-> with – Context manager keyword.

-> open() – Built-in function to open a file.

-> 'output.csv' – String literal for the output filename.

-> 'w' – Mode string meaning "write" mode (creates or overwrites the file).

-> as – Assigns the file object to a variable.

-> f – Variable name for the file object.

-> Purpose – Opens (or creates) a file named output.csv in write mode for saving our CSV data.
<hr>
> Line 13: f.write(output)
<hr>
-> f – The file object opened in the previous line.

-> .write() – A file method that writes content to the file.

-> output – The CSV string we built in the previous lines.

-> Purpose – Writes the entire output string (containing the CSV header and all rows) to the output.csv file.
<hr>
> Line 14: except Exception as ex:
<hr>
-> except – A keyword that handles exceptions (errors) caught by the preceding try block.

-> Exception – A catch-all exception class that captures most types of errors.

-> as – Assigns the exception object to a variable.

-> ex – Variable name (short for "exception") that holds information about the error.

-> Purpose – If any error occurs in the try block, execution jumps here instead of crashing.
<hr>
> Line 15:
<hr>
-> print(f'Error: {str(ex)}')

-> print() – A built-in function that outputs text to the console.

-> f – Indicates an f-string.

-> 'Error: ' – A text string literal.

-> {str(ex)} – An embedded expression.

-> str() – A function that converts the exception object to a readable string.

-> ex – The exception object from the except clause.

-> Purpose – If an error occurs, this prints a user-friendly error message showing what went wrong.
<hr>
✅ What I Learned:-

-> How to read JSON files in Python

-> How to convert JSON data into Python objects

-> How to create CSV formatted strings

-> How to write data into a file

-> How to use loops and f-strings

-> How to handle errors using try-except


