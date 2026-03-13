# Day 1 - Linux Fundamentals Part 1

## Commands

### echo
Outputs any text that we provide.
`echo "Hello"`
- Useful for debugging
- Useful for sending output between commands
- Quotes not needed if there are no spaces in your text

### whoami
Finds out what user we are currently logged in as.
`whoami`

### ls
Lists the files in the current directory.
`ls`
`ls directoryname` - list contents of a directory without navigating to it

### cd
Used to change or jump between directories.
`cd directoryname`
`cd ..` - go back one directory

### cat
Concatenate - outputs the content of a file.
`cat filename`
`cat -n filename` - displays content with line numbers

### pwd
Prints working directory - shows the full file path of where you currently are.
`pwd`

### find
Finds a file in the directory you are in.
`find -name file.txt` - find a specific file by name
`find -name *.txt` - wildcard search, finds anything ending in .txt

### grep
Searches the content of files for a specific value.
`grep "search term" file.txt`
`grep -i "search term" file.txt` - case insensitive search
`grep -r "search term" /var/log/` - search recursively through folders
`grep -n "search term" file.txt` - shows line numbers with results

---

## Operators

### & (Background Operator)
Runs a command in the background of your terminal.
`command &`

### && (AND Operator)
Combines multiple commands in one line. The second command only runs if the first is successful.
`command1 && command2`

### > (Redirect Operator)
Takes the output of a command and directs it somewhere else. Overwrites existing content.
`echo hello > welcome` - creates a file called welcome containing "hello"
- Creates the file if it doesn't exist
- Overwrites the file if it does exist

### >> (Append Operator)
Same as the redirect operator but appends output to the end of a file instead of overwriting it.
`echo hello >> welcome`
- Creates the file if it doesn't exist
- Adds to the end of the file if it does exist

---

## Tips
- `CTRL + L` - clears the terminal
