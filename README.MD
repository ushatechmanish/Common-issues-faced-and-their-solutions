#create a new repository on the command line
echo "# how-to-push-existing-repo-to-github-repo" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ushatechmanish/<your_repo_name>.git
git push -u origin main


#push an existing repository from the command line
git remote add origin https://github.com/ushatechmanish/<your_repo_name>.git
git branch -M main
git push -u origin main

#Push an existing repoistory with various commits to a new github repository 
git remote add origin https://github.com/user/<your_repo_name>.git
git pull origin main --allow-unrelated-histories

## If --allow-unrelated-histories is not included you will get an error that the sources are unrelated 

resolve any merge conflicts by using following methods
1. git status 
To find the files with conflict 
2. Open the files with conflict. You will get something like this 
<<<<<<< HEAD
# Local changes
=======
# Changes from remote repository
>>>>>>> branch-name
3. Remove  >>>>>>> branch-name and <<<<<<< HEAD  pointers and save file after making the required changes 
4. git add . to add conflict files 
5. git push origin main





