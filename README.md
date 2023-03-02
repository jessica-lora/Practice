# Practice GIT

To begin project, if we need to fork a repository:  

One person will need to:  
-fork the original repo (username/password: git personal access token) *skip this step if we do not need to fork the repo*  
-clone the forked repo:  
&ensp;  -in GitHub repo, click on <> code button and copy http text
&ensp;  -in local terminal: git clone `https://github.com/jessica-lora/Practice.git`

-create a develop branch: `git checkout -b develop`  
-push develop branch: `git push origin develop`  

Afterwards everyone else can:  
-clone the forked repo  
-go into develop branch: `git checkout develop`  

-----

*Assuming we have a main branch that we want to leave unchanged until production and want a development branch that we'll push our features branches into*    

To create and work in a feature branch:  
-be in develop branch: `git checkout develop`  
-create feature branch: `git checkout -b feature_name`  
-create files and make changes to code  
-add changes: `git add .`  
-commit changes: `git commit -m"description"`  

Once you complete your commits in the feature branch and are ready to move your feature to develop: you want to update your local develop branch with any new stuff from the develop branch of the online repo (pull: online -> local)  

-switch to develop branch: `git checkout develop`  
-pull into develop branch: `git pull origin develop`   

The next 4 commands will concisely add your feature to the develop branch:  
-`git checkout feature_name`  
-`git rebase develop`  
-`git checkout develop`  
-`git rebase feature_name`  

Update the develop branch online repo with your local develop branch repo updates (push: local -> online):  
-`git push origin develop`  


------

Helpful commands

-`git status` checks the status of files. if the files appear red, they have not beed 'added'; once you do `git add .` and check the status again, they'll appear green

-`git branch` will tell you which branch you are in