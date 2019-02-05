## How to Use Git



### Markdown

[Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


### Setting up SSH key for your personal repository

```shell
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

```shell
Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]

```
At the prompt, for secure passphrase, hit the Enter key. 


Copy your new rsa key to your clipboard


```
pbcopy < ~/.ssh/id_rsa.pub
```


if you don't have pbcopy
```
cat ~/.ssh/id_rsa.pub
```

or 
```
echo ~\.ssh\id_rsa.pub 
```


and copy this from the terminal output.



Follow the instructions to put the ssh key in your github profile

[Add the SSH key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)


## Snippets

### Creating a new repository

```
mkdir project

cd project

git init

git remote add origin git@github.com:yourlogin/your-repo.git


git add .

git commit -am “new repository”

git push -u origin master
```


### Cloning existing repository

git clone https://github.com/username/your-repo.git

Creating branch
git checkout -b feature-1

# you are now in a branch, you can edit and create new files
```
git add .

git commit -am “new feature”
```


Merging branch to master

```
git checkout master

git merge feature-1

git push
```


Deleting branch
```
git branch -d feature-x
```


List all branches
```
git branch -a
```

Switch branch
```
git checkout feature-x
```

Switch to master branch
```
git checkout master
```

Listing Remote repositories
```
git remote -v
```


## Replacing remote repository
in case your remote repository changes, or you want to switch from HTTPS->SSH or SSH->HTTPS

```
git remote remove origin

git remote add origin git@github.com:yourlogin/your-repo.git
```


### resource links


git commands: https://www.atlassian.com/git/tutorials/comparing-workflows/

git flow: http://danielkummer.github.io/git-flow-cheatsheet/

https://www.atlassian.com/git/tutorials/comparing-workflows
