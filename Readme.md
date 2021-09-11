# dumdum

Another trial repo. Initialized locally & pushed to a remote location like GitHub.

- remote means somewhere else, not on this computer. 

- git init
````
path-to-repo\dumdum
λ git init
Initialized empty Git repository in path-to-repo/dumdum/.git/
````

- git remote add origin https://github.com/mahi397/dumdum.git
We use this to add a reference to a remote repository on GitHub.

- git remote -v
Shows any remote repositories that I've connected to this repo.

````
path-to-repo\dumdum (master -> origin)
λ git remote -v
origin  https://github.com/mahi397/dumdum.git (fetch)
origin  https://github.com/mahi397/dumdum.git (push)
````

- git push origin master
To push changes to the remote repo.

- git push -u origin master
To set "upstream", meaning this is where I want to push it by default. So in future, "git push" will suffice.

````
path-to-repo\dumdum (master -> origin)                        
λ git push -u origin master                                          
Enumerating objects: 9, done.                                        
Counting objects: 100% (9/9), done.                                  
Delta compression using up to 4 threads                              
Compressing objects: 100% (5/5), done.                               
Writing objects: 100% (9/9), 985 bytes | 328.00 KiB/s, done.         
Total 9 (delta 1), reused 0 (delta 0)                                
remote: Resolving deltas: 100% (1/1), done.                          
To https://github.com/mahi397/dumdum.git                             
 * [new branch]      master -> master                                
Branch 'master' set up to track remote branch 'master' from 'origin'.
````