# Copy file

- Read [the guideline](https://github.com/mate-academy/py-task-guideline/blob/main/README.md) before start

Write a function `copy_file` that will copy a file in current directory 
like Linux cp command: `cp file.txt file-copy.txt`. Function take only one
argument `command`, that is string with command `cp`, file name to copy and new file
name, separated by spaces.

- It must do nothing in case the user is trying to copy file to file with the same
name.
- Function must copy the whole content to new file.
Example:
```python
copy_file("cp file.txt file.txt")  # Does nothing

copy_file("cp file.txt new_file.txt")
open("file.txt").read() == open("new_file.txt").read()  # True
```
**Note**: It is good practice to use one context manager inside another:
```python
with open(..., "r") as f:
    with open(..., "w") as f2:
        ...
```