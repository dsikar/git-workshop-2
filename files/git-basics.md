# Basic Git commands

**git help** - Getting help
```
$ git help
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one
(...)
```

**git config** - configuration
```
git config --global user.email email@address.com
git config --global user.name "user name"
```

Checking configuration
```
git config --global user.email
git config --global user.name
```

**git clone** - Cloning a repository - note your might need to append your JCI User ID to git repository URL

```
$ git clone https://jsikard@github.jci.com/jsikard/git-workshop.git
Cloning into 'git-workshop'...
remote: Counting objects: 39, done.
remote: Compressing objects: 100% (35/35), done.
remote: Total 39 (delta 9), reused 18 (delta 3), pack-reused 0
Unpacking objects: 100% (39/39), done.
```

Note you will probably be asked for a username and password.  

![Authentication](../images/authenticating.png)

Changing directory into repository
```
$ cd git-workshop
```

**git remote** information about the remote repository
```
$ git remote
origin
```

Verbose switch -v
```
$ git remote -v
origin  https://jsikard@github.jci.com/jsikard/git-workshop.git (fetch)
origin  https://jsikard@github.jci.com/jsikard/git-workshop.git (push)
```

**git branch** - What branch are we working on?
```
$ git branch
* master
```

Show remote branches
```
$ git branch -r
  origin/master
```

**git log** - Show logs
```
$ git log
commit d9c9b4848004088596ccca72215e9727d225cff6 (HEAD -> master)
Author: Daniel Sikar <daniel.sikar@jci.com>
Date:   Tue Aug 7 09:43:55 2018 +0100

    Added image.

commit 6f88293c73851825709d65cb5661285214465f6f (origin/master)
Merge: 0f8ae9b 67b4052
Author: Daniel Sikar <daniel.sikar@jci.com>
Date:   Tue Aug 7 09:11:54 2018 +0100
```

## LAB 1

1. Open Git-Bash and change directory to ~/Documents
```
$ cd ~/Documents
```
2. Create jci-git directory
```
$ mkdir jci-git
```
3. Change directory to jci-git
```
$ cd jci-git
```
4. Configure your email address and user name 
```
$ git config --global user.email JCIGlobalID@jci.com - note use your own JCI email address, name in quotes 
$ git config --global user.name "My Name"
```
5. Check configuration
```
$ git config --global user.email
$ git config --global user.name
```
6.  Clone a repository - note you might have to append your JCI Global ID to URL like such https://jsikard@github.jci.com/jsikard/git-workshop.git
```
$ git clone https://github.jci.com/jsikard/git-workshop.git
Cloning into 'git-workshop'...
remote: Counting objects: 39, done.
remote: Compressing objects: 100% (35/35), done.
remote: Total 39 (delta 9), reused 18 (delta 3), pack-reused 0
Unpacking objects: 100% (39/39), done.
```
7. Change directory to git-workshop
```
$ cd git-workshop
```
8. Inspect files
```
$ ls -last
```
9. Find out where remote repository is
```
$ git remote
origin
```
10. Use **verbose -v** switch for added information
```
$ git remote -v
origin  https://jsikard@github.jci.com/jsikard/git-workshop.git (fetch)
origin  https://jsikard@github.jci.com/jsikard/git-workshop.git (push)
```
11. Show the branches that exist in your local repository
```
$ git branch
```
12. Show branches that exist in the remote repository
```
$ git branch -v
```
## Adding (Modifying repository), Staging and Committing files. Checking logs and deleting files.

**git status** - current repository status
```
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

Adding a file to repository

```
$ ls > files-ds.txt
```

**git status** - current repository status (Modified)
```
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        files-ds.txt

nothing added to commit but untracked files present (use "git add" to track)
```
**git-add** - Add files to "Staging" area

```
$ git add files-ds.txt
warning: LF will be replaced by CRLF in files-ds.txt.
The file will have its original line endings in your working directory.
```

**git-commit** - Commit file to repository
```
$ git commit -m "Added files-ds.txt"
[master f46d0d4] Added files-ds.txt
 1 file changed, 4 insertions(+)
 create mode 100644 files-ds.txt
```

**git-push** - Push modifications to remote repository
```
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 376 bytes | 188.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.jci.com/jsikard/git-workshop.git
   3664d3d..f46d0d4  master -> master
```

## LAB 2

Adding, staging, commiting and pushing.  

1.  Change directory to git-workshop if not there already
```
$ cd git-workshop
```
2. Add a file (Modify repository)
```
$ ls > files-<your-initials>.txt
```
3. Add to Staging area
```
$ git add files-<your-initials>.txt
```
4. Commit 
```
$ git commit -m "Added files-<your-initials>.txt"
```
5. Push to remote repository 
```
$ git push
```
6. For good measure, check last 5 log entries (-5 switch)
```
$ git log -5
```

## Next week we will look at branching and merging features as well as **git init** and deleting files

**git init** - Initialise a repository, list hidden files in chronological and size descending order (-last)

```
$ cd ~/Documents/jci-git/
$ git init multi-mx-simulator
$ cd multi-mx-simulator
$ ls -last
```

Notes, git repositories can be moved around like any set of files, sent as zip file, copied to pen drive, etc.  




