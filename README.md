Takes an input string or file and outputs its MD5 hash.

##Examples:
Any arguments will be interpreted as strings. Each argument will be interpreted as a separate string to hash, and will be given its own output (in the order of input).
```
$ ./md5 "Hello, World!"
65a8e27d8879283831b664bd8b7f0ad4

$ ./md5 "Multiple" Strings
a0bf169f2539e893e00d7b1296bc4d8e
89be9433646f5939040a78971a5d103a

$ ./md5 ""
d41d8cd98f00b204e9800998ecf8427e

$ ./md5 "Can use \" escapes"
7bf94222f6dbcd25d6fa21d5985f5634
```
If no arguments are given, input is taken from standard input.
```
$ echo -n "Hello, World!" | ./md5
65a8e27d8879283831b664bd8b7f0ad4

$ echo "Hello, World!" | ./md5
bea8252ff4e80f41719ea13cdf007273

$ echo "File Input" > testFile | ./md5
d41d8cd98f00b204e9800998ecf8427e

$ cat testFile | ./md5
7dacda86e382b27c25a92f8f2f6a5cd8

```
As seen above, it is important to note that many programs will output a newline character after their output. This newline *will* affect the output of the MD5 algorithm. `echo` has the `-n` flag that prevents the output of said character.

If entering input by hand, end collection of data by entering an EOF character (Ctrl+D in some cases).
