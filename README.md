To config your name: git config –global user.name “Your Name”
To config your email adress: git config –global user.email Email
To check this info: git config –global --list
Type: clear to clear every thing
To create the default branch “main” : git config –global init.default branch main
git init  initialized local git repository on your device
to change main branch name: git branch -m master main
git status, to check status of our repo
to track a file: git add filename
to untrack a file: (use "git rm --cached <fileName> ”
to track all files: git add .  OR git add -A   OR git add –all

After changing a file, you can type: git diff to see changes have been made

-----
In order:
-	Changing files  working files environment
-	After you “git add” the changed files  staging environment
-	After you “git commit” the changed files  commit environment
To stary tracking of the file  git add …
To add it to history  git commit …
git restore --staged <file> and git rm --cached <file> both unstage files
to automatically stage files that have been modified and to just commit the changes  git commit -a -m “Comment”
to delete a file git rm filename or “file Name”
after you have directly did that if you want to restore it 1- git restore --staged filename 2- git restore filename
to rename a file  git mv “oldName” “newName”
git log  to see all different commits or git log –oneline
git commit -m “New Comment” --amend: command is used to modify the most recent commit message

to go back to a commit: git reset hashtag 

to edit the view of commit history: git rebase -i –root

We create another branch so we can work on whatever we want to work on, not causing an effect on the main branch, then when we are sasitfied with our work, we can merge our branch with the main branch. The new branch is essentially a snapshot of the current state of the original branch(main) at the time of its creation.

To create a new branch: git branch branchName.
To confirm how many branches you have: git branch
to switch to a branch: git switch branchName

When you are sasitsfied with the changes you made in the other branch, you can now merge the other branch with the main branch. If you want to merge branch1 into branch2, you need to be on branch2 when you run the merge command: git merge -m "comment" branchToMerge

to delete a branch: git branch -d branchName

#Stopped at merge conflicts#

To create and switch to a new branch: git switch -c branchName

When a merge conflict happens, open the file and leave the version you want and delete the version you don’t like, then commit the changes.

-----------------------------------------------------------------------------------------------------------------
Typical flow on git to work on a feature or a bug:
1-	Create your own branch
2-	Make your changes
3-	Merge it back to the main branch
4-	Delete the branch that you were working on

GitHub:
1-	git remote add origin https://github.com/username/repository.git --> Purpose: Allows you to push and pull changes between your local repository and a remote repository hosted on GitHub or another Git server.
2-	 git branch -M main  Purpose: Helps standardize the primary branch name to main, aligning with modern Git practices and conventions.
3-	git push -u origin main, Purpose: The command git push -u origin main is used to upload your local branch's commits to the remote repository on GitHub to set up a tracking relationship between your local branch and the remote branch.


to pull the changes from the remote branch: git pull origin main

to push all branches to git hub: git push –all

After editing files locally, you need to push the changes back to git hub, using git push origin branchNameYouArePushingFrom

When you create a pull request, you are requesting that someone reviews and merges your changes from one branch into another branch of the repository, typically from a feature branch into the main branch

After making edits on gi t hub, to show it locally you need to  Fetch updates from the remote repository. This updates your local copy of the remote branches but does not alter your local working directory. 
1- git fetch origin
2- git pull origin <branch-name>
