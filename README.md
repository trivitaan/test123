# test123

## Sekedar Catatan kumpulan command git via cmd

##ini test
##triv
##triv#2

See What Branch You're On

    Run this command:
        git status

List All Branches

NOTE: The current local branch will be marked with an asterisk (\*).

    To see local branches, run this command:
        git branch
    To see remote branches, run this command:
        git branch -r
    To see all local and remote branches, run this command:
        git branch -a

Create a New Branch

    Run this command (replacing my-branch-name with whatever name you want):
        git checkout -b my-branch-name
    You're now ready to commit to this branch.

Switch to a Branch In Your Local Repo

    Run this command:
        git checkout my-branch-name

Switch to a Branch That Came From a Remote Repo

    To get a list of all branches from the remote, run this command:
        git pull
    Run this command to switch to the branch:
        git checkout --track origin/my-branch-name

Push to a Branch

    If your local branch does not exist on the remote, run either of these commands:
        git push -u origin my-branch-name
        git push -u origin HEAD

NOTE: HEAD is a reference to the top of the current branch, so it's an easy way to push to a branch of the same name on the remote. This saves you from having to type out the exact name of the branch!

    If your local branch already exists on the remote, run this command:
        git push

Merge a Branch

    You'll want to make sure your working tree is clean and see what branch you're on. Run this command:
        git status
    First, you must check out the branch that you want to merge another branch into (changes will be merged into this branch). If you're not already on the desired branch, run this command:
        git checkout master
        NOTE: Replace master with another branch name as needed.
    Now you can merge another branch into the current branch. Run this command:
        git merge my-branch-name
        NOTE: When you merge, there may be a conflict. Refer to Handling Merge Conflicts (the next exercise) to learn what to do.

Delete Branches

    To delete a remote branch, run this command:
        git push origin --delete my-branch-name
    To delete a local branch, run either of these commands:
        git branch -d my-branch-name
        git branch -D my-branch-name
    NOTE: The -d option only deletes the branch if it has already been merged. The -D option is a shortcut for --delete --force, which deletes the branch irrespective of its merged status.
