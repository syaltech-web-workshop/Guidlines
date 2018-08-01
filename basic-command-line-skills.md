# Basic Command Line Skills
## Navigating the file system
- Navigating the file system using command line is similar to navigating between your directories(folders) using your regular file explorer except that you are not using mouse to click on desired folder, Instead you type commands to tell where you need to go from here.
- Next is a list of commands that should be useful when navigating the file system using Command Line:
### pwd
` where you need to go from here `

The pwd command is related to the `here` part in this sentence. As the sentence implies if you need to go somewhere you must be somewhere. So this command is used to print the Current Working Directory(Where you are now in your filesystem)

This command takes no arguments, Meaning it doesn't require to write something else after it in the terminal. Just write it and hit enter and you get the output of it.

### cd
So after knowing where you are standing with ` pwd ` command you want to go somewhere else, In other words you need to change the Current Working Directory. It accept one argument (the path of the directory) which can be relative or absolute , . This furthermore takes us to two common terms "relative path" and "absolute path".
##### But what's a path first
The path is the location of a directory or file in the filesystem.

When someone asks you where the pics of last summer and he tells you: : Enter "D" then "pics" then "summer" and you will find the pics in a folder named 2017. Then the path of the pics is "D:\pics\summer\2017".

##### Absolute Path vs Relative Path
"D:\pics\summer\2017" is an "Absolute path", Meaning it's self descripted and relative to any other thing.

While "Relative Path" is the path related to your current working directory. So if your current working directory is "D:\pics" then the relative path of last summer pics in this example is "summer\2017".

##### Dot (.) and Double Dot (..)
- The dot symbol (.) inside a path means the current directory. ``` cd pics ``` and ``` cd ./pics ``` are the same as they both change your current directory into pics raltive to your current directory now at the moment of running the command. The only difference is that when you say ``` cd ./pics ``` you are telling explicitly that this is the path relative to my current directory and this might be useful in some situations.
- The double dot symbol (..) inside a path means "up one level". That if your current directory is "D:\users\xyz" and you run the command ``` cd ../users/abc ``` then your current working directory "D:\users\abc"

Unlike (.) that usually appear single time in the start of a path, (..) can appear multiple times and may appear in the middle or the end of the relative path. 

An Example of (..) in the middle: Given an absolute path ``` D:\users\xyz\dir1 ``` then a path relative to it like ``` dir2\..\..\dir3 ``` will have an absolute path of ``` D:\users\xyz\dir3 ```

##### Examples of using cd
- Your current working directory is "D:\pics" and you need to go to the last summer pics directory with cd command
    - Using relative path ``` cd summer\2017 ``` or ``` cd .\summer\2017 ```
    - Using absolute path ``` cd D:\pics\summer\2017 ```
  
  As you realize using cd with absolute path is independent of your current working directory if you need to access some directory using its absolute path you will type the same command wherever you are in the file system

- Your current working directory is "C:\users\xyz" and you need to change it into "C:\users"
  - ``` cd .. ```
- Your currnet working directory is "C:\users\xyz\dir1" and you need to change it into "C:\users\xyz\dir2"
  - ``` cd ../dir2 ```
  
##### Linux vs Windows
- One of the common differences between windows and linux's filesystem is the beginning of any absolute path in linux is "/" which means the root of the filesystem. While in windows every absolute path should start with a drive letter like "D:" and "C:"
- Another difference is the special character that separates directory names inside a path. In linux it's a forwared slash "/", While in Windows it's a back slash "\". But don't worry when working using Cmder terminal integrated into laragon you can use either because it emulates the command line evironment in linux.

## Creating files using the command line

- echo "SOME TEXT" > file.txt

Will create a file.txt with "SOME TEXT" inside it, You can use ``` echo "" > file.txt ``` to create an empty file

- touch file.txt

It will create an empty file too

## Creating directory using the command line
- mkdir dir_name

## Removing a file 

- rm file_name

## Removing an empty directory
- rmdir dir_name

## Removing a directory that contains files
- rm -rf dir_name

