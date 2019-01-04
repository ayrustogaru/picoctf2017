#### Question:
>We found an even bigger directory tree hiding a flag starting at /problems/d9fbdb968961f708989999193aaca05d. It would be impossible to 
>find the file named flag manually...

#### Hint:
>Is there a search function in Linux? Like if I wanted to 'find' something...


#### Solution:
Use the *find* command:
```
find /problems/d9fbdb968961f708989999193aaca05d -type f -name flag -exec cat {} \;                                            
e553af78ff1f7a6a428456ac53d837e5
```

`-type f` - Find a file

`-name flag` - with the name flag

`-exec cat {} \;` - print out the contents of the file

`{}` is used as a placeholder for `find`'s `-exec`. The `-exec` command is terminated with a semicolon (`;`), which should be escaped (`\;`) to avoid interpretation by the shell.
