# Working with git (and GitHub)

#### Download git ([https://git-scm.com/downloads](https://git-scm.com/downloads))

- This will allow you to use git locally in a command-line or GUI interface

- It will work with any repository system using git version control (GitHub is the most common)

- During install, make sure you set the options to interface with git using Git Bash. This will mean you can use git with a dedicated command line interface (called the “Git Bash” shell)

- Once installed, open the Git Bash shell:

  ![gitbash](E:/git/VA_NH_docs/img/gitbash.png)

There are a couple important global settings you'll want to set the first time you use Git Bash. These include your name and e-mail address, and the default text editor to open when needed. Set these with the following commands.

```
git config --global user.name "John Doe"

git config --global user.email john.doe@domain.com

git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

The last command sets Notepad++ as the default text editor. You can change to whatever editor you'd like by altering the path.

In git bash, you can navigate and manipulate your file/folder system using basic commands. The most important is `cd`, which is used to change the current directory. For example, if you create a folder `E:/git` to hold all of your git repositories locally, you can navigate to it with:

```
cd E:/git
```

All git-commands start with a `git` call, e.g., `git pull`. In Git Bash, you can view most useful git commands with the call:

```
git --help
```

## Starting with a new, local repository

Any folder can be initialized as a new git repository. For example, to create a new **local** repository `VA_NH_docs` to store this document and other helpful tools for the organization, we can use the commands:

```
git init VA_NH_docs 
```

That creates a new folder, which we now navigate to:

```
cd VA_NH_docs
```

Git bash will now indicate that you are in a git repository, since it will show the current branch you are using (by default in a new repostory, this is called `master`) in parentheses in blue lettering.

You can now add folders/files to this repository. For example, this document `intro_git.md`  and associated images can be added to the folder. It's also a  good idea to always create a  `README.md` file directly in a repository folder, which will automatically display on the main repository page on GitHub. 

#### Link local repository to a remote

Once you're ready to add the repository to GitHub, you'll need to create a new, completely empty repository on GitHub (the **remote**) there with the same name (`VA_NH_docs`) as the local repository. 

Once it's created, we can tell git where the remote GitHub repository is located:

```
git remote add origin https://github.com/VANatHeritage/VA_NH_docs.git
```

This tells git to add a new remote repository link, with the name `origin`. This only needs to be done once for each remote (generally, you'll only have one, always named `origin`).

#### Add and commit changes locally

Now we can **add** and **commit** the changes we've made to the repository locally. Adding *stages* the changed files, while committing finalizes the changes to a tagged and commented **commit**.

You can add one file/folder at a time, or add all changed files using `*`.

```
git add *
```

You can view the current status of your repository at any time by typing the command `git status`. If you run it after the previous add command, you'll see that all files are ready to be committed, and you can do so with:

```
git commit
```

A new text editor window should pop up, where you can add a message (details) to the commit. An empty message will abort the commit, so make sure to write something.

#### Push local changes to the remote

Finally, you can **push** these committed changes to the remote repository:

```
git push
```

Now the remote repository is up-to-date with our local one. 

## Working with an existing repository

When you want to start working on the repository again, open Git Bash and navigate to the local repository (e.g., `cd E:/git/VA_NH_docs`), and then use:

````g
git pull
```

to **pull** the changes from the remote to our local repository, which would incorporate any changes that were made by other users. The use the process outlined above:

- make any edits to files/folders
- use `git add *` to *stage* all of the changes locally
- use `git commit` to *commit* all the changes locally
- use `git push` to *push* all the changes to the remote repository

#### 

