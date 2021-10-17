# How to git

Lets try to get one starting point on our local machine from a repo and learn about git along the way.

### What is a repository?
Just a "Folder" on a remote location (in this case GitHub)

-Repo has branches (like *main*)
-There can be more than one branch

### Forking a repository ([Learn more](https://docs.github.com/en/get-started/quickstart/fork-a-repo))
-What is a fork?

It's not a spoon, fork is a copy of a repository. Forking a repository allows
you to freely experiment with changes without affecting the original project. 
(Link to a discussion on Why we use forking? 
content:
In our case we want to provide the starting point of a Lab assigment. 
You just fork it and work on it. We can all see eachothers forks and changes in them. Ask questions and so on)

-[How to do it?](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository)


### Cloning
-What is cloning?
In simplest terms, you copy a repository on to your local device.

-[How to clone?](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository)

short: open GitBash/cmd/powershell... and cd [cmd command] into a folder you want to clone the repo in.

run ```git clone <clone https link>```
**Nice!**

You now have a local repo that you cloned. What now?

## Let's start with basics
run ```git status```
- This shows you the current branch and it's state

run ```git branch```
- This shows you all the local brances. `-r` shows remote repos. `-a` shows them all. (On GitHub).
note: branch named origin/<any branch name> is remote. [See what origin means](https://www.git-tower.com/learn/git/glossary/origin)

### Jump to an another branch
When you know the name of the branch you would like to go to.

run ```git checkout <branch name>```

- #### Tip: cmd doesn't have auto fill with tab. Powershell and GitBash do *#USE TAB*

-"There is no branch I want locally!"

run ```git fetch --all``` and try again.  
If it existed on the remote, local will now know.

### Create a new branch 
When creating a new branch you copy a current one and make a new instance of it.

run ```git checkout -b <branch name>```
-It will create a new branch and put you on it.
run ```git status``` 
-if you want to see all info agian (dont be afraid to use it)

### Making changes on a branch
Create a change on a branch (create a file *it can be anything*)
- #### Tip: git ignores empty folders. Or you can add an empty .gitkeep file to any folders you want included.

run ```git status``` and you should notice a change.
- *Changes are not **staged** yet*

### Staging changes
Before we can commit our changes we need to stage them.
run ```git add <file name to be staged>```
- to add a specific file
or 
run ```git add .```
- to stage all changes

### Commiting changes
Think of this like a package with new changes that you will put a label on.
Later you can always access this package (commit) and see what was changed in it

run ```git commit -m "your cool message"```

- if it all went smoothly you should have a commit to see all commits 
run ```git log```
- this command will show you all the info about all the commits that were made on this branch and parent branches
- The term ```HEAD``` refers to the current commit you are viewing and on what branches it is
- `commit dajf9z28f3zfad9safhuifh33fua...` it's commits actual name (a hash). 
- ### Tip: hash is important if you start using git more often. Usefull af
- and you see a label message of a commit

Now you have commits on your local repo.

### Pushing local commits on the interwebs (remote repo)

run ```git push```
- you will probably get an error
```fatal: The current branch newbranch has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin <branch name>```

##### Why?
You are trying to push a new branch you created localy. That branch doesn't exist remotly
Git doesn't know where to put your commits, but git is great and he knows what you should do.

```git push --set-upstream origin <branch name>```
- [find out what this is (Recommended)](https://stackoverflow.com/questions/18031946/what-does-set-upstream-do)

### View remote
You can go on GitHub and navigate to a branch you just pushed

##Congrats! If you are stuck or have any questions, or ideas. Please don't hesitate and start a discussion.
we will gladly help eachother.
