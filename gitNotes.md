# Reviewing GitHub

> 1/8/20  
> Review through Acha

## Working on Local Server

## What a Commit does
* Committing takes efficient snapshots of your entire project 
* `Commit` command will add a file to the GIT folder (=repository)  in your project folder start keeping track of versions - all on your own drive 
    * You must include a message
    * The program will keep track of author and commit time etc
    * Git uses a hashing algorithm called **SHA** to compare the files in it to the files in the project folder, and can let you know if any files are “dirty”, aka they have changes that haven’t been committed
        * A hashing algorithm like SHA can have a set length output hash that can be large enough that the probability that two files of different values will have the same hash is absolutely miniscule

## Using Git from the shell
* Start with `git init` command, that will create a folder on your home drive containing all the metadata/tools git will use
* Use the `git add [file name]` command to the *stage* to be ready to go in one commit, and ` git commit` to 
* Use `git checkout [branch name]` to go a version to work on

## Branching
* *“Master”* is an alias pointing to the very latest version of project - holds the hash code of that snapshot
    * You can create similar aliases for other commits called *“tags”*
* Branches are a way to test out different solutions or pathways in work simultaneously. Go up branches and to parents to go back versions
    * Think of this as a replacement to having to comment out sections of your code when trying different solutions to a problem
    //“Head” is the version that you’re working on. If you go to a previous version and work experimentally there, “head” changes to the hash of that version
When you merge = git will create a new version copying the old master and integrate the changes made in the specified branch. That new version has two parents - the old master and the branch og
Conflicts can occurs bween branches on same fule

Working with others on github
Use “push” and “pull” to add and remove the repository to github, using the url provided there (pulling grabs a copy of the onlline repository)
You can add tags and branches too


