# Useful Git Commands


1.  `git remote -v `// List all remote repositories
2.  `git remote add origin`// + repository link - This adds a new remote to an existing project
3.  `git checkout -b anyName `//Creates a new branch called anyName and move to it
4.  `git push --delete <remote_name> <branch_name> `// Deletes remote branch
5.  `git branch -d <branch_name>`// Deletes Local Branch
6.  `git branch -a `// List all the remote branches
7.  `git merge <:branch_you_want_to_merge:>`// Merges the branch_you_want_to_merge to the branch your are in
8.  `git diff `// Show changes between HEAD and working directory
9.  `git log -S 'LoginViewController' `// Show commits that make add or remove a certain string
10. `git log --oneline`// Show the list of commits in one line format
11. `git log — all — grep=’day of week’ `// Search commits that contain a log message
12. `git remote rename old new `// Rename remote
13. `git branch branch_name sha1_of_commit `// Create branch from commit
14. `git branch -m old new `// Rename other branch
15. `git branch -m new `// Rename current branch
16. `git reset --hard HEAD~1 `// Undo last commit
17. `git cherry-pick 12944d8 `// Get Commit
18. // Change Commit Message after push
```
git commit --amend -m "New commit message"
git push --force <repository> <branch>
```

19. // Squash last n commits into one commit
```
git rebase -i HEAD~5
git reset --soft HEAD~5
git add .
git commit -m "Update"
git push -f origin master
```

20. `git branch | grep -v "master" | xargs git branch -D` //Delete all local branches but master
21. `git branch -r | awk -F/ '/\/PREFIX/{print $2}'` //Do a dry-run first to see the branches that you want to remove
22. `git branch -r | awk -F/ '/\/PREFIX/{print $2}' | xargs -I {} git push origin :{}` //Remove Remote branches that share the same prefix | Replace PREFIX
