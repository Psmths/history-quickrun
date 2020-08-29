# history-quickrun
 Quickly find and run past commands from bash history. This is a python script that will take user input and use regular expressions to match it to commands found in your bash history. It will then return an enumerated list of the commands it found and allow you to run the one you were looking for instead of abusing the up arrow key.

 # Usage
```
./hr 'partial command'
```

The input argument being a regex can be used to search for multiple commands:

```
./hr 'sys|echo'
```

Additionally, the script allows you to run a chain of commands successively by entering a comma separated list of indices such as 3,7,13.

It should be noted that the current shell session history is stored in memory, whereas this program reads from a history file. In order to update the history when the command is run you may consider setting an appropriate alias such as:

```
alias h='history -a; hr $1'
```
