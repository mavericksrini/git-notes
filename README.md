# git-notes

## To create a branch off of an upstream branch (non-master)
For those git projects that maintain several version branchnes, it's necessary to apply fixes to all version branches. 
The below creates a branch from an upstream branch including the feature along with upstream branch name
```
git checkout -b restart-logic-php54 origin/php54
```
You then makes the changes and push to your fork. After which, you create a PR to merge your new branch into the upstream one.
## Deleting local and remote branches
```
$ git push -d <remote_name> <branch_name>
$ git branch -d <branch_name>
```
Note that in most cases the remote name is origin
