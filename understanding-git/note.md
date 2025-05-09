#### Git is distributed Version control system

- ###### Version control mean the power to go back to your previously written code ,previous version of the current code allowing you to manage and restore earlier states of your project.

###### Centralized version control system:it is a version control model where all the versions of a project are stored in a single central server.

###### Distributed Version Control System (DVCS) is dominant because the complete version history is stored both on your local computer and on a remote server.

- ###### This allows you to work independently without needing a constant internet connection, and easily collaborate with other developers when needed.

- Command Line prompt:

  - git config --global user.name "Anannya" : Sets your git info
  - git config --global user.email "gshgsa@main.com" : Sets your git info
  - git config --global --list : Shows your details
  - git init : It creates a hidden .git folder where Git stores all the tracking information and changes for the project.
  - git status : To check the current branch
  - git add <file_name/folder_name> :It stages the specified file or folder.
  - git rm --cached <file_name/folder_name>: It unstage the specified file or folder.
  - git log : Shows all the commit in past of the directory
  - git commit -m "commit message":It commits your staged work to the local repository.

  - git commit -a -m "commit message":It automatically stages all the modified (tracked) files and commits them to the local repository.
  - git diff : It shows the changes between the files in the working directory and the staging area (i.e., what you have modified but not yet staged).
  - git diff --staged: After you stage changes, git diff won't show them. To see the differences between the staged files and the last commit, use git diff --staged.

- Staging Area : If you want Git to track changes to a specific file, you need to add that file to the Staging Area.
- Commit History :It is a record of everything you have staged and committed so far.
- working directory:This is where you add files, create directories, and implement changes. To let Git track these changes, you need to stage the files first.
- when you update something in the file,it gets updated in working directory not Staging Area.
- When you delete something from your working directory,you must check if it's already push to git .If it is then remove it from git first.(e.g : git rm --cached understanding-git/cred.txt)

##### Command to map local repository with remote and push the files using ssh

###### Step-by-step history

- 1 ls
- 2 ls -a
- 3 ssh-keygen -o ( Generate a new SSH key pair)
- 4 ls -a
- 5 cd # Go to home directory
- 6 ls -a
- 7 cd .ssh (Navigate to the .ssh directory)
- 8 clear
- 9 ls -a
- 10 cat id_rsa.pub (Copy the public key)
- 11 history

###### Link local repo to GitHub using SSH

- 12 git remote add origin git@github.com:AnannyaDeveloper404/springboot-projects.git
- 13 git push -u origin main

##### Why SSH : Using SSH allows you to securely connect to GitHub without needing to enter your username and password every time you push or pull. It works by verifying that the SSH key on your local machine matches the public key stored in your GitHub account.

##### GIT TAG : It refers to a specific version or snapshot of the complete project, often used to mark release points (e.g., v1.0, v2.0).

##### Annotated tag: A tag that stores additional information such as the tagger’s name, date, message, and is saved as a full Git object.

##### Lightweight tag: A simpler tag that only points to a commit without any extra metadata or message.

- Command Line prompt for tag:
  - git tag : shows all the tags for a specific repo
  - git tag -a v1.0 -m "1st release" :It adds tag or specify the release point of the product
  - git push origin v1.1 : pushing the tag or release point to the remote repo.
  - git log --pretty=oneline : It shows the summary of commits
  #### Before merging make sure to pull origin main

##### BRANCHING COMMAND LINES and steps to add branch and committing it and pushing it to the remote repo

- git checkout -b <branch-name> - create a new branch
- git switch -c <branch-name> - create a new branch
- git checkout <branch-name> - switch branches
- git switch <branch-name> - switch branches
- git commit -m "<message>"
- git push origin <branch-name>- e.g, features1,features2 or main
