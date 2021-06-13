# [Git Submodules] (https://www.git-scm.com/book/en/v2/Git-Tools-Submodules)

## Adding a repo as submodule

NOTE: Make sure folder name is using "_" not "-" for Python repositories. Else importing it becomes a problem

1) Add the submodule
```
$ git submodule add https://github.com/YOUR_USERNAME/YOUR_SUBMODULE_REPO
```

2) Check git status.
```
$ git status
> new file:   .gitmodules
>	new file:   YOUR_SUBMODULE_REPO
```
2 new files should automatically be staged.

3) Commit these files and push.
4) The submodule with the COMMIT_ID should appear in your Github repo.


## Removing a submodule after adding it to the repository
If possible try and avoid this situation and make sure you add the submodule correctly. 

1)  Remove the submodule entry from .git/config
`git submodule deinit -f path/to/submodule`

2) Remove the submodule directory from the superproject's .git/modules directory
`rm -rf .git/modules/path/to/submodule`

3) Remove the entry in .gitmodules and remove the submodule directory located at path/to/submodulegit 
```
rm -f path/to/submodule
git reset HEAD .gitmodules`
rm .gitmodules
```

## Submodule updates 

Here we will be making changes in a repository and then including the updates in another repository where it is used as a submodule.

### Submodule Repository
1) Make changes in the code. 
2) Commit and Push.
3) Note the commit id.

### Repository where submodule is used
1) Open terminal inside the submodule folder
``` 
git fetch
git log --oneline origin/master -10
git checkout LATEST_COMMIT_ID 
```
LATEST_COMMIT_ID should be the same as the one noted before.

If the above commands gives a message like detached HEAD then you might want to do git pull instead
