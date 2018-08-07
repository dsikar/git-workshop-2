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

**git clone** - Cloning a repository - note your repository url might be different
```
$ git clone https://jsikard@github.jci.com/jsikard/git-workshop.git
Cloning into 'git-workshop'...
remote: Counting objects: 39, done.
remote: Compressing objects: 100% (35/35), done.
remote: Total 39 (delta 9), reused 18 (delta 3), pack-reused 0
Unpacking objects: 100% (39/39), done.
```

Note you will probably be asked for a username and password.  


