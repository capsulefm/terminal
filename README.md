terminal
========

A go-native terminal handler for reading a line with history.

A fork of *bitbucket.org/binet/go-terminal* which forks *code.google.com/p/go.crypto/ssh/terminal*

It allows editing a line with arrow keys, and history using up/down arrow keys.

bitbucket.org/binet/go-terminal added some history.

This repo fixed/adds:

*  functions to set up from stdin/out
*  history line slice copying bug
*  and history list getting/setting.

**Usage:**

```go 
term := terminal.NewWithStdInOut()  
term.ReleaseFromStdInOut() // defer this  
term.SetPrompt(prompt string)  
term.ReadLine() (line string, err error)  
term.ReadPassword(prompt string) (line string, err error)  
term.SetHistory([]string)  
term.GetHistory() (h []string)  
term.Write(buf []byte) (n int, err error)  
```
