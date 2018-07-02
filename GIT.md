# Helpful notes take when using git

## Using forked model
This would have a master repository (upstream) in your organization and you 
would fork it into your github profile repositories. Clone from the forked 
(origin) to your local. Commits and then push would be to your profile's
forked repository, then you create a pull request to have it merged back
into upstream.  To keep you local repository up to date you pull (or fetch
then merge) from upstream. 

## Creating a repository
Create your reposity on github. Once completed you can clone the empty 
repository, then copy existing code into the repository, then add,
commit, and push.

## Use .gitignore file to not track certain file types
Use .gitignore file to disregard certain files types, an example would be the
.project file placed in the code directory by eclipse.

## GIT commands
### Clone a repository
To get code from github to your local drive you clone the repository. To clone
a repository issue the command git clone URI 
(https://github.com/yourusername/repository.git). An example would be 
https://github.com/ncelwell/Sandbox.git.  Note you can also get this URI from 
the repository Clone or download button in GitHub.

### Shows remote URIs
To verify you have correctly set the URIs to your origin (and upstream if using
forked workflow) issue the command git remote -v. Sample output:
Notes> git remote -v
origin	https://github.com/ncelwell/Notes.git (fetch)
origin	https://github.com/ncelwell/Notes.git (push)

If I wanted to add an upstream remote, the command would be:
git remote add upstream https://github.com/YourOrganization/Notes.git, for 
example git remote add upstream https://gitnhub/contractlandstaff.com/Notes.git

### Track changes
To tract changes modifed, new or deleted files use the command git status
Notes> git status
On branch master
Changes not staged for commit:

	modified:   README.md

Untracked files:

	.gitignore
	GIT.md
Files that are not commited and modified are README.md and new files that are
not commited are .gitignore and GIT.md

### Add files to be staged for commit
To add files to be staged for your next commit, issue the command"
git add your_filename (or use wildcard to add all *), for example,
git add GIT.md to just add the one file or git add * to add all files.

### Commit your files (record changes in your local repository)
To record the changes in you local repository issue the command:
git commit -m "Your commit message here"

## Push your files (record changes in your remote repository)
To push changes to the remote repository on the master branch issue the 
command: git push origin master
