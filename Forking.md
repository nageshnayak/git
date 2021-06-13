# Setting up the Repository
These steps are needed once to setup the repository. All the steps below are given for an example repository https://github.com/daplab-iitb-children-speech-dataset/iitb-lexicon.

## Step 1: Fork the main upstream repository
1) Create a fork of the [main upstream repository](https://github.com/daplab-iitb-children-speech-dataset/iitb-lexicon) in your private github account (origin repository).
2) Clone the forked version from your origin repository to your local machine and use this version.
3) Check if you have done steps 1 & 2 successfully by listing the current configured remote repository for your fork. Open terminal from within the local repository folder and type:
```
    $ git remote -v
    > origin  https://github.com/YOUR_USERNAME/iitb-lexicon (fetch)
    > origin  https://github.com/YOUR_USERNAME/iitb-lexicon (push)
```
`origin` should have the url for your forked version of the repo.

If you see `https://github.com/daplab-iitb-children-speech-dataset/iitb-lexicon` instead, it means that you have cloned the upstream repository instead.

## Step 2: Configuring the upstream
1) Open Terminal.

2) Specify the remote upstream repository that will be synced with the fork.
```
    $ git remote add upstream https://github.com/daplab-iitb-children-speech-dataset//iitb-lexicon
```

3) Verify the new upstream repository you've specified for your fork.
```
    $ git remote -v
    > origin    https://github.com/YOUR_USERNAME/iitb-lexicon (fetch)
    > origin    https://github.com/YOUR_USERNAME/iitb-lexicon (push)
    > upstream  https://github.com/daplab-iitb-children-speech-dataset/iitb-lexicon (fetch)
    > upstream  https://github.com/daplab-iitb-children-speech-dataset/iitb-lexicon (push)
```


# Suggesting changes to be merged with main repository (Committing changes and opening a pull request)
1) If there are any changes, first create a new branch. Master branch will be used to synchronize with the upstream repository.
2) Commit any changes to the new branch and push. You may need to set an upstream branch. These will be pushed to origin/BRANCH_NAME.
3) In your github repository, it will show that your branch is 'X' commits ahead. There will be an option next to this "Contribute". Clicking on it will give another option "Open Pull Request". Click on it and then "Create Pull Request". 
4) Post this it will inform you if there are any conflicts and if automatic merging can be performed on not. Check the differences and confirm if the changes are valid. If yes then tap on "Create Pull Request". 
4) Next it will show a screen with your commit message and a button "Create pull request". Click on it. This will create a pull request which will then need to be merged by the Repository Manager.
5) In case there are some comments are made by the Manager regarding the commit which needs to be fixed before merging, you can keep updating the code and committing on the same branch (No need to create a pull request again) till the commit is merged by the Manager.


# Merging in the main repository (Only for the Repository Manager)
1) Open the upstream repository in github and go to "Pull requests".
2) Click on the Pull request.
a) In case there are no conflicts, it will state "This branch has no conflicts with the base branch". 
b) In case of conflicts, "Resolve conflicts". Delete the conflict markers <<<<<<<, =======, >>>>>>> and make the changes you want in the final merge. 
c) If there are any issues/comments these can be made using the "Conversations(General)/Files changed(Specific lines in files)" section. More commits can be made to the same branch post which merging can take place.
3) Choose "Merge pull request" with the "Squash and Merge" option. This ensures only last commit is part of the main repository.


# Syncing local repository with updates made in the main repositry (Fetch and Merge upstream repository locally)
1) Once a particular branch has been merged into the main repository, the remote branch may be deleted. 
2) Post this, you will need to sync your main branch to the master branch of the main repository so that you can use this for your work.
```
git checkout main
git fetch upstream
git merge upstream/main
```
This will get your local repository updated with the latest changes in the upstream repository. This needs to be periodically done when changes in the repository are notified.
