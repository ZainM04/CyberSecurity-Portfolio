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


## Secure Shell (SSH)
SSH is a protocol used to connect to and interact with the command line of a remote Linux machine. Communication is encrypted.

`ssh username@IP_address`

---

## Flags & Switches
Most commands allow additional arguments identified by a hyphen followed by a keyword, known as a flag or switch.

`ls -a` - shows hidden files and folders

### Getting Help
`command --help` - lists possible options and brief descriptions for a command
`man ls` - opens the manual page for the ls command
- Press `q` to exit the manual page

---

## Commands

### touch
Creates a new empty file.
`touch filename`
- Only takes one argument — the file name
- Use `echo` or `nano` to add content to the file after creating it

### mkdir
Creates a new directory or folder.
`mkdir foldername`
- Only takes one argument — the directory name

### cp
Copies a file or folder and its entire contents.
`cp sourcefile destinationfile`
- Takes two arguments — the file to copy and the name to assign the copied file

### mv
Moves or renames a file or folder.
`mv filename destination`
- Takes two arguments — the file name and the destination
- To rename: use the new name as the second argument instead of a destination path

### rm
Removes a file or folder.
`rm filename`
`rm -R foldername` - removes a folder and everything inside it
- Be careful — there is no recycle bin in Linux, deletion is permanent

### file
Determines the type of a file.
`file filename`
- Takes one argument — the file name

### cat (additional note)
Can be used to view the contents of a file.
`cat filename`

---

## File Permissions
Every file and folder has permissions that determine who can read, write, or execute it.

`-rwxrwxrwx`

| Section | Meaning |
|---------|---------|
| First bit | `-` for file, `d` for directory |
| First `rwx` | Permissions for the file owner |
| Second `rwx` | Permissions for users in the same group |
| Third `rwx` | Permissions for every other user on the system |

### Permission types
- `r` - read
- `w` - write
- `x` - execute

---

## Switching Users

### su (Substitute User)
Switches to another user account.
`su username`
`su -l username` - simulates a full login as that user, inheriting their environment variables and properties

---

## Common Directories

| Directory | Purpose |
|-----------|---------|
| `/etc` | Stores system configuration files used by the operating system |
| `/var` | Stores data frequently accessed or written by running services and applications |
| `/root` | Home directory for the root user |
| `/tmp` | Temporary directory — volatile, cleared on restart. Used for data only needed once or twice |

---

## Tips
- `CTRL + L` - clears the terminal
