# Reviewing GitHub

> 1/8/20  - 1/15/20
> Review through Acha :yellow_heart:

# Working on Local Server

## Using Git from the Command Line
* Start with `git init` command, that will create a folder on your home drive containing all the metadata/tools git will use
* Use the `git add [file name]` command to the *stage* to be ready to go in one commit, and ` git commit` to 
* Use `git checkout [branch name]` to go a version to work on
* Use `git log` to see the files in your repository so far
* A shortcut to use instead of adding and committing a change seperately is `git commit -am "[insert message]"`

## What a Commit does
* Committing takes efficient snapshots of your entire project 
* `Commit` command will add a file to the GIT folder (=repository)  in your project folder start keeping track of versions - all on your own drive 
    * You must include a message
    * The program will keep track of author and commit time etc
    * Git uses a hashing algorithm called **SHA** to compare the files in it to the files in the project folder, and can let you know if any files are “dirty”, aka they have changes that haven’t been committed
        * A hashing algorithm like SHA can have a set length output hash that can be large enough that the probability that two files of different values will have the same hash is absolutely miniscule

## Branching
* *“Master”* is an alias pointing to the very latest version of project - holds the hash code of that snapshot
    * You can create similar aliases for other commits called *“tags”*
* Branches are a way to test out different solutions or pathways in work simultaneously. Go up branches and to parents to go back versions
    * Think of this as a replacement to having to comment out sections of your code when trying different solutions to a problem
* *“Head”* is the version that you’re working on. If you go to a previous version and work experimentally there, “head” changes to the hash of that version
* When you merge = git will create a new version copying the old master and integrate the changes made in the specified branch. That new version has two parents - the old master *and* the og branch 
* Conflicts can occurs bween branches on same file - sometimes git will take a decision (like if one branch's file is empty), sometimes it will throw an error and make you manually integrate the changes.

# Working on Github
* Once you have a repository made on your computer, go to your profile and create a repo/ find a repo you're adding to, and get the address to paste into your command line. You should see smth to paste in like this;
    * `git remote add origin https://github.com/lizageorge/LearningGit.git`
    * `git push -u origin master`
* Use `push` to add to the *origin* repository, and `pull` to copy from it
* When pushing from your own computer, you can transfer the tags and branches you made too
* You can use GitHub to work with others, just as you can with any server. GitHub just happens to be publically available
**Distributed Version Control System** = unlike a *Local VCS*, where all the work and access to it is stored on one main server and the owner of that server has a lot of control/power, in a DVCS every user can “act like the server” but everyone has equal access to the work. 	
* Also, to confirm identities when committing/pulling work, use a **public-private key**


# The Process of Working on a Team
1. Clone the team's remote repository onto your desktop
2. Create the branch for your feature (if the lead didn't alreay create it for you)
3. Work on your own branch to complete the feature. Periodically merge the master branch or your teammate's branches into yours to avoid major conflicts later on
4. Once you're done working, do one last merge from master and resolve any conflicts. Then create a pull request/ask your lead to review the changes to merge into the master branch
5. Have an ice cream and congragulate yourself on finishing the work :D