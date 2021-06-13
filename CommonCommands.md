### Intitialize a empty repository
Inside the folder where you would like to initialize the repository, open Terminal and type
```
$ git init
```
### Cloning 
#### Existing repository
```
$ git clone https://github.com/YOUR_USERNAME/YOUR_REPO LOCAL_REPO_FOLDER_NAME(Optional)
```
#### Latest commit contents only
```
$ git clone --depth 1 --recurse-submodules --shallow-submodules https://github.com/YOUR_USERNAME/YOUR_REPO LOCAL_REPO_FOLDER_NAME(Optional)
```
### Git Log History with commit IDs
```
$ git log
```
### Status of current repository (Files unchanged, modified, staged)
```
$ git status
```
### Adding files to staging
```
$ git add FILE_PATH_NAME
```
### Unstaging changes
```
$ git reset HEAD <file>
```
### Commiting staged files with a commit message
```
$ git commit -m "COMMIT_MESSAGE"
```
### Setting up a remote (Github)
1) Open your github account
2) Create a new repository
3) Follow steps mentioned in "pushing existing repo from the command line"
```
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY
git branch -M main
git push -u origin main
```
### Pushing changes to remote
```
$ git push
```
### Checking difference of modified files
```
$ git diff
```
### Checking differences of staged files
```
$ git diff --staged
```
