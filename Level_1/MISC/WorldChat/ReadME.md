#### Question:
>We think someone is trying to transmit a flag over WorldChat. Unfortunately, there are so many other people talking that we can't 
>really keep track of what is going on! Go see if you can find the messenger at shell2017.picoctf.com:61161. Remember to use Ctrl-C 
>to cut the connection if it overwhelms you!

#### Hint:
>There are cool command line tools that can filter out lines with specific keywords in them. Check out 'grep'! You can use the 
>'|' character to put all the output into another process or command (like the grep process)

#### Solution:
1. Connect to the IP and use `nc shell.2017.picoctf.com 61161 | grep flag`.
2. Observe the output, the flag is printed out in parts such as `this is part 1/8 of the flag - 1a2e`.
3. Use the pattern as follows:
```
nc shell.2017.picoctf.com 61161 | grep -e "this is the part [0-9]\/8 of the flag"
```
4. Join all the parts of the flag.
