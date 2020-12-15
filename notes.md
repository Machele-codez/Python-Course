# Python Course
This course is intended to allow you to understand the fundamentals of python and working with it on a local environment up to the point of at least building mini-apps that run in the command line. SO first of all we start with the CLI and work our way through basic programming terminology, Python itself, data types, functions, files, exception handling all the way to classes and objects in Python

# CLI
The command line interface is an alternative way to the GUI which allows us to manipulate the computer. The GUI uses graphics; images, gestures, text, etc. whereas the command line basically uses commands. So they do the same thing but in different ways. CLI might give you more or easier access to deeper functionality from what I know, at least. 

## Terminal
For a GUI, to issue commands you would primarily use the mouse buttons or the keyboard. For the CLI, you'd have to literally type out whatever you want to the computer to do for you. These are called commands. The CLI can be accessed via programs called terminals (or shell or console). Examples of terminals are
- Command Prompt
- Power Shell
- Terminal
- Termux

For this tutorial we'll be using Command Prompt and then maybe Power Shell. So let's launch CMD which is short for command prompt.

## Files
A file is basically a resource for recording data. The file can be an executable, meaning it can be run, like a game or a software installation. It can also be a video, a Word document, audio, or picture.

## Directory
A directory is like a container where you can store your files and other directories on your PC. So, a directory is also known as a folder. 

## Parent Directory
The parent directory is the folder in which another folder is found

## Path
When you open Command Prompt you realize that there's some blinking underscore. Yes, that's the cursor. It indicates where you type your commands. 

Before the cursor, there's something like:
```shell
C:\Users\machele-pc>
```
That is called the path. The path is telling you the folder in which you have opened the terminal. So right now we are in a folder called `machele-pc`. And `machele-pc` is a subfolder of the `Users` folder. 

So the parent directory of `machele-pc` is `Users`. 

`C` is the name of our drive (drive letter) that's why it ends with a colon "`:`". 

><!-- TODO --> So let's open the file explorer and see if we can go to the same location that we are in in our terminal. 
><!-- TODO  --> Open the file explorer and show the path in the address bar too.

## dir
The dir command lists the contents of a directory. When used alone it lists the contents of the current directory. To list the contents of a directory we can first `cd` into it then `dir`. Or we can simply `dir` the path to that directory. 
So, to list the contents of the preceding directory, we can simply type `cd ..`



><!-- todo --> Illustrate this by opening two terminal windows. `dir` another directory using relative path in one window and dir the same directory by first cd-ing into it.

**NB:** 

`.` stands for the current directory.

`..` stands for the previous directory.

## chdir or cd
`cd` stands for change directory. It is similar to using the mouse to double-click a folder. It updates the path in the terminal indicating that you have moved into a different folder. So remember, the path keeps track of your current location (the folder you are in). How is it used? Simple!
```shell
cd FolderName
```
```shell
cd "FolderName With Spaces"
```
Remember `.` and `..`

Therefore executing the following command:
```shell
cd ..
```
should send change your directory to the one before the current one in the path.

And executing the following command:
```shell
cd .
```
should not really do anything.

## mkdir or md
`mkdir` stands for "make directory". It is a command used to create a new directory / folder. Just type
```shell
C:\Users\machele-pc\Tests> mkdir newHere
```
to create a folder called `newHere` in the `Tests` folder. 
You can also create multiple sub-directories at once. 
Let's say we are in a directory called `Tests` and we want to create a folder called `One` and inside `One` we want to create `Two`. We can simply do this;
```shell
C:\Users\machele-pc\Tests> mkdir One\Two
```

## rmdir or rd
`rmdir` is used just like `mkdir`. It is used to remove or delete a directory. When executed alone (without flags), it can only remove empty directories. Supposing `Two` is an empty directory:
```shell
C:\Users\machele-pc\Tests\One> rmdir Two
```
If you want to use it to remove a directory that contains files and other directories then you'd have to add the `/S` flag. Supposing `Three` is not empty. 
```shell
C:\Users\machele-pc\Tests\One> rmdir /S Three
```

### So what is a flag?
Well, a flag is simply a way of executing a command and adding options. So with a flag, you can customize the way the command is executed. For example, if you use the `/S` flag with the `rmdir` command you can see that it modifies the command and allows it to delete not only the folder specified, but also its subfolders and files.

## help
As the name implies, help is a command used to show more information about the built in Windows commands. It shows you how to use the command and the flags that the command can be used with. 

*Usage*
```shell
help command
```

## echo
`echo` can be used to just display text on the screen
 ```shell
echo hello there
```
 or save text to a file.
 ```shell
echo hey there > greet.txt
```

## del
`del` is used to delete a file.
 ```shell
del greet.txt
```
