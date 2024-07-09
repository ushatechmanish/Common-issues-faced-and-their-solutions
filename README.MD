# How to Push an Existing Repo to a GitHub Repo

## Create a New Repository on the Command Line

    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/ushatechmanish/your_repo_name.git
    git push -u origin main


# push an existing repository from the command line

    git remote add origin https://github.com/ushatechmanish/your_repo_name.git
    git branch -M main
    git push -u origin main


# Push an existing repoistory with various commits to a new github repository 
    git remote add origin https://github.com/user/your_repo_name.git
    git pull origin main --allow-unrelated-histories


Note: If --allow-unrelated-histories is not included you will get an error that the sources are unrelated 

# resolve any merge conflicts by using following methods
1. To find the files with conflict 
  git status 
1. Open the files with conflict. You will get something like this 

    ```<<<<<<< HEAD     
    # Local changes     
    =======     
    # Changes from remote repository     
    >>>>>>> branch-name```
1. Remove ```>>>>>>> branch-name and <<<<<<< HEAD```  pointers and save file after making the required changes 

1. git add . to add conflict files 

1. git push origin main
