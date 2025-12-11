# GIT and GITHUB

## GIT install in ubuntu
```bash
sudo apt update
sudo apt install git
git --version  # for verification
```

## GIT configuration
```bash
git config --global user.name "<username>"
git config --global user.mail "<usermail>"
git config --list  # verify username and email
```


## usecase: push your local project to git
- It should not be a git repository

```bash
cd <projectname>
ls   # to see all the files
la   # to see all the dot file
```
## Initialize git
```bash
git init
la   #you'll see a new .git folder
```
## Create a .gitignore file
- this helps you avoid accidentally committing unwanted or secured or large files
```bash
touch .gitignore
echo ".venv/" >> .gitignore
echo ".env/" >> .gitignore
```
## check for new files
```bash
git status
```

## to add files to staging area to be tracked
```bash
git add <filename>   #add single file to git
git add .            # to add all files, it is risky so don't do it
git status            # to check file is added to stage area
```
## commit with a proper message
```bash
git commit -m "descriptive-commit-message"
```

## Create a repo in GITHUB 
### if you already having a git repo, to get it........
- open GITHUB account
- open that repository, click on code button, copy https path

### To create a git repo in github freshly
- open GITHUB account
- there you will fine new repository button, proceed to create a new repo
- after created new repo, click on code button
- copy https path

## to connect project to GITHUB
```bash
git remote add origin <paste the https path that copied from repo in GITHUB>
```

## to push your project to GITHUB
```bash
git push -u origin <branchname> #for first git push, add -u
git push orgin <branchname>
```

## branch
```bash
git branch #to check current branch
git branch <new-branch-name> #to create a new branch and not to switch
git checkout -b <new-branch-name> #creates a new branch and switch to new branch
git checkout <branch-name> # to switch to another branch
```

