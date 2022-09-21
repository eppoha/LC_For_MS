Steps to renaming local and remote branches
Let’s achieve the result with the steps described below:

Renaming local branch to the new name
To rename the local branch to the new name, use the git branch command followed by the -m option:

git branch -m <old-name> <new-name>

To delete the old branch on remote (suppose, the name of remote is origin, which is by default), use the following command:

git push origin --delete <old-name>

Or you can shorten the process of deleting the remote branch like this:

git push origin :<old-name>

Pushing the new branch to remote
Then you should push the new branch to remote:

git push origin <new-name>

To reset the upstream branch for the new-name local branch use the -u flag with the git push command:

git push origin -u <new-name>

Branching
Git branches are an important part of the everyday workflow. Branches are a pointer to a snapshot of the changes you have made in Git. Branching helps cleaning up the history before merging it. Branches represent an isolated line of development. They are considered as a way to request a new working directory, staging area, and project history. The isolated lines of development for two features in branches make it possible to work on them in parallel and make the master branch free from questionable code. The git branch command creates, lists and deletes branches not allowing to switch between branches or put a forked history back together.

Local and Remote Branches
The local branch is a branch existing on the local machine. It can be seen only by the local user. The remote branch is a branch on a remote location. A remote-tracking branch is a local copy of a remote branch. Assuming a newly-created <NewBranch> is pushed to origin using the git push command and -u option, a remote-tracking branch named <origin/NewBranch> is created on your machine. The remote-tracking branch tracks the remote branch <NewBranch> on the origin. Update and sync the remote-tracking branch with the remote branch using the git fetch or git pull commands. A local tracking branch is a local branch tracking another branch. Local tracking branches mostly track a remote-tracking branch. When pushing a local branch to the origin with git push -u, the local branch <NewBranch> tracks the remote-tracking branch <origin/NewBranch>.