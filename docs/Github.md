# Github guide

## Creating a new repository  
Create the folder where you want your code to be, then cd into it and type:  

```
$ git init
```

## Working on somebody elses repository  

```
$ git clone [path to repository]
```

## Common Worklow  
The first step of committing code to git is to stage the code. Its a fancy word meaning you pick the files to include in your commit.  

To get an idea of what changed, you Use the status command which lists the files that have changed:  

```
$ git status
```

Next, you can diff one of the files you have made changes to in order to see line by line what has changed:  

```
$ git diff <filename>
```

If you want to revert the file back to its original state and revert your changes, you use the checkout command:  

```
$ git checkout <filename>
```

If you are happy with the changes in the file, you have to add it to your commit.  

```
$ git add <filename>
```

Now, if you hit git status again, you will notice that the file you changed is green. This means you can commit this file.  

If you change your mind and want to exclude a file from your commit you can use the reset command. Keep in mind that this does not revert the file, its just like saying, 'I want to keep working on this file, but dont want it in my commit'.  

```
$ git reset <filename>
```

You are now ready to commit the file, which will save the current state of the file to your local repository..  

```
$ git commit -m "Describe your commit here"
```

Congrats! Now youve committed the file, but it wont show up in github -- just on your local computer.  

To sync the commit to origin (github), you use a command called push:  

```
$ git push origin master
```

This pushes your local commits to the branch called `master` to a destination called `origin`.  

But what happens if somebody else has committed code to the repo? Then git would ask you to pull first. If you work on a repo with others, its good habit to first run the pull command before doing a push:  

```
$ git pull origin master
```

This pulls in new commits from origin (github) into your local git repo.  

Sometimes you want to be able to see all the commits to your repo, thats when you use the log command:  

```
$ git log
```

To make it look nicer you can do:  

```
$ git log --graph --oneline --decorate --all
```


## Advanced Workflow

.. Will add information on branching later.

