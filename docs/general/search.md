# Searching

The search bar found in many of the table views supports regular expressions.

When you enter a search term and press Enter, all of the visible columns in the view are included in the search.

## Common Searches Patterns

### Begins With `^`

Example:

Firstly, we search for `PSUB-` and note that many rows are returned that contain `PSUB-` in either the Part# or Allocated column.
![alt text](image.png)

To narrow the search to just `PSUB-` Part#s, we can add the begins with regex pattern `^` to the search term:
![alt text](image-1.png)

### Ends With `$`

Search for `0477`:  
![alt text](image-2.png)

Ends with `0477`:  
![alt text](image-3.png)

!!! tip
    If you want to search for a `$` or `^`, you need to escape it with `\`  
    Eg. `\$` will return rows that have columns containing `$` in their text.

### Match Any Character `.`

`.+` One or more characters:  
`CAP-.+`


### Examples

Begins with `CAB` and ends with `REV A`: `^CAB.+REV A$`  
![alt text](image-4.png)
