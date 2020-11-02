# Guide on technical content PH
This repo is a guideline on how to change rakwireless-doc-internal repo for Technical Content PH team.

_____

## A. How to run a local dev server via YARN

### Go to the directory of your local repository.

This is just an example. Check your own directory.

    cd documents/rakrepo/rakwireless-docs-internal

If you have no local clone yet, execute 

    git clone git@github.com:RAKWireless/rakwireless-docs-internal.git*  

It is private so you should have access on it using your Rakwireless github account.
    

### Initialize modules: 

    yarn install 
    
### Run the local dev server:

    yarn docs:dev
    
____

## B. Steps on proposing new change on rakwireless-docs-internal repo using PH-Review branch.

Go to the directory of your local repository. If you have no local repo yet, go to section A how to clone one.

### Have an updated copy of PH-Review branch from the repo by doing

    git checkout PH-Review
    
followed by

    git pull
    
This will ensure that your are updated with PH-Review. This is very important to have a clean pull request later.


### Create a new branch where you can work on your changes

    git checkout -b <name-of-my-review-branch>	

As an example, I will name it rak811-add-images

    git checkout -b rak811-add-images

### Check if your current branch is pointing to the one you newly created.

    git branch 

### You can now change the files that needs improvement using your favorite editor like VSC, vim, brackets, etc.

You can view the updated rakwireless doc on the local dev server you created on *section A* or if MD preview plugin is available on your editor.

### After doing the improvements on the docs. You need to add it on the staging area. All those added will be included on the commit.

To check the list of files you’ve changed via git, you can use 
    
    git status
    
After double checking the changed files, you can now add the file changes on the staging area.

    git add <path/filename>
    
You can also use 

    git add . 

to add all files you’ve changed. This saves time on adding changed files.

### Commit the changes if you are now 100% sure on the change.

Before doing any commit, ensure that you are really updated with the PH-Review branch. Always remember that PH-Review branch is constantly changing. This is critical to have a clean pull request later.

    git pull origin PH-Review

You are now ready to commit!

    git commit -m “this is quick summary of the changes made”.

Please put a meaningful comment that reflects the changes you've made.

### Push now your local branch to github repo of rakwireless

    git push origin <name-of-my-review-branch>

### You are ready now to do a pull request.

It is advisable that you do immediately a pull request after you perform a push. This is to avoid any commits that will overlap on your changes. The master repo is constantly changing as well as the PH-Review. You don't want any pull request with commits from other people. Though git will manage this, it is better if we have a clean pull request.

Only the files changed should be the ones on the actual commit. It should not include any changes from other files you didn't change. We always have to ensure that we have a clean pull request.


