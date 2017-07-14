# Working with git (and GitHub)

#### Download git ([https://git-scm.com/downloads](https://git-scm.com/downloads))

- This will allow you to use git in a command-line interface

- It will work with any repository system using git version control (GitHub is the most common)

- During install, change the setting to interface with git using Git Bash. This will mean you can use git with a dedicated command line interface (the “Git Bash” shell)

- Once installed, open Git Bash

  ![gitbash](E:/git/VA_NH_tools/img/gitbash.png)

In git bash, you can navigate and manipulate your file/folder system using basic commands. The most important is `cd`, which is used to change the current directory. For example, if you create a folder `E:/git` to hold all of your git repositories locally, you can navigate to it with:

```
cd E:/git
```

All git-commands start with a `git` call, e.g., `git pull`. In Git Bash, you can view most useful git commands with the call:

```
git --help
```

#### Starting with a new repository

Any folder can be initialized as a new git repository. For example, to create a new repository `VA_NH_tools` to store this document and other helpful tools for the organization, we can use the commands:

```
git init VA_NH_tools 
```

That creates a new folder, which we now navigate to:

```
cd VA_NH_tools
```



