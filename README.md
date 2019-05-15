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

## Make a new branch after commiting locally to master (oops)

You can create a new branch whenever you want. After you had committed your changes, you could run:
```
$ git checkout -b my-branch
```
The above would create a new branch named my-branch based on the current commit. If you want to revert the master branch as part of this operation (that is, you want your changes only on the new branch, not on the master branch) you can do this:

```
  # create a new branch, but don't switch to it
  git branch newbranch

  # Reset current (master) branch by discarding the most recent
  # commit.
  git reset --hard HEAD^

  # Switch to new branch
  git checkout newbranch
```
And now you can push your new branch to the remote server.
