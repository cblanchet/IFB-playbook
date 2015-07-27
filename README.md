# IFB-playbook
 This repository is to store ansible playbooks 
 to build [IFB](http://www.france-bioinformatique.fr/) appliances
 set up by Institut Pasteur.
 **This NOT the official repository for all IFB appliances.**

## How to contributes

 If you want to start contributing to this repository, 
 you definitely need to install git and create a GitHub account.

### Creating a GitHub account


### Get a copy of this repository
 
 If you are logged in to GitHub, you can go to the IFB-playbook
 repository page and click on a button named 'Fork'. 
 This will create a fork (basically a copy) of the official IFB-playbook repository, 
 publicly viewable on GitHub, 
 (in document below we will call this repository "upstream" whereas your won github copy
 will called "origin").

 Now, assuming that you have git installed on your computer, 
 execute the following commands locally on your machine. 
 This "url" is given on the github page for your repository (if you are logged in):

`git clone git@github.com:yourusername/biopython.git`

 You have just created a local copy of the IFB-playbook repository on your machine.
 You may want to also link your local repository with the  bioinfo-center-pasteur-fr/IFB-playbook
 (see below on how to keep your copy in sync)

`git remote add upstream https://github.com/bioinfo-center-pasteur-fr/IFB-playbook`

 If you haven't already done so, tell git your name and the email address you are using on github 
 (so that your commits get matched up to your github account). For example,

```
git config --global user.name "David Jones"
git config --global user.email "d.jones@example.com"
```

### Keep your copy in sync with upstream

 Don't actually make any changes to the master branch in your local repository (or your fork on github). 
 Instead, use named branches to do any of your own work. 
 The advantage of this approach it is the trivial to pull the upstream master 
 (i.e. the bioinfo-center-pasteur-fr/IFB-playbook)
 to your repository.

 Assuming you have issued this command (you only need to do this once):

`git remote add https://github.com/bioinfo-center-pasteur-fr/IFB-playbook.git upstream`

 Then all you need to do is:

```
git checkout master
git pull upstream master
```

Provided you never commit any change to your local master branch, 
this should always be a simple fast forward merge without any conflicts. 
You can then deal with merging the upstream changes from your local master branch 
into your local branches (and you can do that offline).

Then push the updated local master branch to the github origin repository:

`git push origin master`

### Making changes locally.

Now you can make changes to your local repository - you can do this offline, 
and you can commit your changes as often as you like. 
In fact, you should commit as often as possible.

**First of all**, create a new branch for **each** new playbook you want to add or modify, and switch to it.
	
```
git branch my_new_playbook
git checkout my_new_playbook
```

### Pushing changes to Github

Once you think your changes are stable and should be reviewed by others, 
you can push your changes back to the GitHub server:

`git push origin my_new_playbook`

*only the core developers will have write access to the main repository.*

### Submitting changes for inclusion in bioinfo-center-pasteur-fr/IFB-playbook

On GitHub itself, you can inform keepers of the main repository of your changes by sending a 'pull request' 
from the main page of your github repository.

It is mandatory to merge with the current trunk of IFB-playbook (i.e. the bioinfo-center-pasteur-fr/IFB-playbook's master branch),
or better yet rebase to the current trunk, before submitting your changes to avoid excess work on the receiving side. 

**before submitting** any pull request, please sync your repositories with upstream 
to avoid conflicts and avoid excess work on the upstream side.


