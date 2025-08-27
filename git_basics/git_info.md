### Git

Git is a version control system that helps us to track the changes that we make to code and allows for collaboration among multiple developers.

Check if git is installed in your system. Open a terminal in vs code and type below command. It will output the version onumber of git installed in your system. 

```
git --version
```

Use below command to check where git is installed, it will output the path of executable file of git
```
where.exe git
```

### Git Setup

- Setup username and email

```
$ git config --global user.name supriya-s-jadhav
$ git config --global user.email supria005@gmail.com
```
Without the --global option, this setting will only apply to a specific repository.

- Remove files from version control tracking

```
$ echo <filename> >> .gitignore
```

Add the paths of files under the .gitignore file. Git will no longer manage those files. You will have to commit the .gitignore file for this to work

-Display settings

```
$ git config --global --list
```

Initialize a new git repository from local
```
git init
```

clone a git repository to local
```
git clone 'repository_link'
```

list all branches in the repository; with the option -a, it will show all branches including remote
```
git branch
git branch -a
```

Create new branch, referencing the current HEAD.
```
git branch branch_name
```

Switch working directory to the specified branch. With -b: Git will create the specified branch if it does not exist.
```
git checkout -b branch_name
```


Remove selected branch, if it is already merged into any other. -D instead of -d forces deletion.
To delete the local branch, use one of the following:
```
git branch -d <branch_name>                 # Delete local
git branch -D <branch_name>                 # Delete local
git push -d <remote_name> <branchname>      # Delete remote
```

Remove file from working directory and staging area.
```
git rm [file]
```


### Remove .DS_Store files

To remove .DS_Store files from a Git repository, you'll need to follow these steps. .DS_Store files are created by macOS Finder and are typically not needed or wanted in a Git repository as they are specific to macOS file management.


#### Removing Existing .DS_Store Files

1. Delete .DS_Store Files Locally

Navigate to Your Repository: Open your terminal or command prompt and navigate to your Git repository.
```
cd /path/to/your/repository
```

Remove .DS_Store Files: 

Use git rm with the -cached option to remove .DS_Store files from the Git index (but not from your file system to avoid deleting them locally):
```
git rm --cached '*.DS_Store'
```

This command removes .DS_Store files from the Git staging area/index. The *.DS_Store pattern matches all .DS_Store files in the repository.

2. Commit the Changes

Commit the Deletion: Commit the changes to remove .DS_Store files from the Git repository:

```
git commit -m "Remove .DS_Store files from repository"
```

3. Verify Changes

Push Changes (if needed): If you have already pushed these files to a remote repository, you might want to push the removal commit:

```
git push origin <branch-name>
```
Replace <branch-name> with your branch name.

#### Prevent Future .DS_Store Files

1. Ignore .DS_Store Files Globally

Create or Edit .gitignore File: Open your text editor and create a .gitignore file in the root of your Git repository if it doesn't already exist:
```
nano .gitignore
```

Add .DS_Store to .gitignore: Add the following line to .gitignore to ignore .DS_Store files:
```
.DS_Store
```

Save and Close the File: Save the .gitignore file and close your text editor.

2. Apply .gitignore Changes

Commit .gitignore File: Add and commit the .gitignore file to your repository:
```
git add .gitignore
git commit -m "Add .gitignore to ignore .DS_Store files"
```

Push Changes (if needed): If you've made changes to .gitignore, push the changes to the remote repository:
```
git push origin <branch-name>
```



### References:

- [Github Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Git Commands](https://git-scm.com/docs)