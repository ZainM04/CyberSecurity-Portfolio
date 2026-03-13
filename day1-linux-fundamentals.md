##Day 1 (Morning Block) - Linux Fundamentals Part 1 
Linux Commands:

Echo - Outputs any text that we provide (Echo "Hello")
You would use the echo command for debugging 
It is also useful for sending things between commands 
If you don't have spaces in your text you don't need to include quotations

whoami - Find out what user we are logged in as 

ls - listing, lists the files in the current directory
you can list the contents of a directory without having to navigate to it by using ls and the name of the directory 
 
cd - used to change or jump between directories 
to go back a directory use the command (cd ..) 

cat - concatenate, outputs the content of the file 
 
pwd - prints working directory 
This command is used to find the full file path of the working directory 

find - Will find a file in the directory you are in 
If you know the file name you would use a command like (find -name file.txt) 
You can use a wildcard (*), this allows you to search for anything that ends in what you specify. (find -name *.txt)

grep - allows us to search the content of files for specific values what we are looking for 
An example of a grep command is (grep "Search" file.txt)


Linux Operators: 
& - Allows you to run commands in the background of your terminal 
Known as the background operator

&& - Allows you to combine multiple commands together in one line of your terminal 
The second command will only run if the first command is successful 

> - It is a redirector, means we can take the output from one command and direct is somewhere else 
(echo hello > welcome) this command would print hello and make a file called welcome to print "hello" to 
If the file exists the redirector will over write the content of the file 
If the file doesn't exist the redirector will make the file 

>> - This operator is the same as the redirector, but appends the output rather then replace it 
This is an known as the appending operator. This is also a redirect operator 
Instead of rewriting a file, this operator just puts the output at the end 


Tip: 
CTRL + L, this clears the terminal 
