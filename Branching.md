# Git Branching

- git branch: to list out all branches in your repo. The one marked with * is the current working branch.
````
path-to-repo\dumdum (master -> origin)
λ git branch
* master
````

- git checkout -b branch-name : -b is used to create a new branch
````
C:\Users\HP\Desktop\dumdum (master -> origin)        
λ git checkout -b feature-branch                     
Switched to a new branch 'feature-branch'            
````
````                               
C:\Users\HP\Desktop\dumdum (feature-branch -> origin)
λ git branch                                         
* feature-branch                                     
  master                                             
````
- git checkout branch-name : to switch to branch-name branch