## Steps to follow after making contributions

1. Fork the repo
2. Clone the repo
3. If owner has already created a branch for the issue, then use it, else create a new branch
4. Make the changes
5. Add the changes to the index
6. Commit the changes
7. Push the changes to the forked repo in the feature branch
8. Create a pull request
9. Wait for the owner to review the pull request
10. If the owner is okay with the changes, then he/she will merge the pull request
11. If you want to delete the branch locally, then use `git branch -d <branch_name>`
12. If you want to delete the branch remotely, then use `git push origin --delete <branch_name>`
13. If any contributor has already make new changes to the same branch or any other branch, then use `git fetch upstream --prune` to fetch the changes  
    This will remove all the old changes and will make the new changes in `upstream` to be reflected in the local repo
    - If you want to update the remote forked repo or clean the deleted branches, you can also use `git fetch origin --prune`
    - You'll use `git fetch --all --prune` to synchronize all the remote repositories
14. If you want to update the forked local repo with the latest changes, then use `git pull upstream <branch_name>`
15. Lastly, you should use `git push origin <branch_name>` to push the changes to the forked repo

<br>

## Steps to take to do it from GitHub

1. Fork the repo
2. Clone the repo
3. If owner has already created a branch for the issue, then use it, else create a new branch
4. Make the changes
5. Add the changes to the index
6. Commit the changes
7. Push the changes to the forked repo in the feature branch
8. Create a pull request
9. Wait for the owner to review the pull request
10. If the owner is okay with the changes, then he/she will merge the pull request
11. If you want to delete the branch locally, then use `git branch -d <branch_name>`
12. If you want to delete the branch remotely, then use `git push origin --delete <branch_name>`
13. Click `Sync fork` in the forked repo from GitHub
14. Use `git fetch upstream --prune` and `git fetch origin --prune`
15. Use `git pull origin main` to update the local forked repo with the latest changes
16. Make your new features and `git push origin <branch_name>`
17. Make a PR

<br>

## Delete Last Commit

There're 3 ways to delete the last commit with:

- `git reset --soft HEAD~1`  
  Deletes the last commit  
  It keeps the changes in the staging area (it means, the changes are ready to be committed)
- `git reset --mixed HEAD~1`  
  Deletes the last commit  
  It keeps the changes in all the files  
  But they're not in the staging area  
  💬️ **Note**: this is the default behavior of `git reset HEAD~1`
- `git reset --hard HEAD~1`  
  Deletes the last commit  
  Deletes the changes in the staging area
  Also deletes the changes in all the files  
  📌 **Important**: your project will return to the previous commit state
