#### Question:
>I heard you have some "delusions of grandeur" about your typing speed. How fast can you go at shell2017.picoctf.com:44840?

#### Hint:
>Use the nc command to connect! I hear python is a good means (among many) to generate the needed input.
>It might help to have multiple windows open.

#### Solution:
May not be the recommended solution but this is what I've done:

1. Fire up the terminal from your desktop.
2. Use the *nc* command to connect to the mentioned IP and port `shell2017.picoctf.com:44840`. You would get an output like this
```
To prove your skills, you must pass this test.
Please give me the 'z' character '517' times, followed by
 a single '5'.                                           
To make things interesting, you have 30 seconds.         
Input:
```
3. Type in the desktop terminal, according to the question, `python -c "print 'z'*517 + '5'"`
4. Copy and paste this into the terminal. Be as fast as possible ;).
