# Git Branching

- git branch: to list out all branches in your repo. The one marked with * is the current working branch.
````
path-to-repo\dumdum (master -> origin)
λ git branch
* master
````

- git checkout -b branch-name : -b is used to create a new branch
````
path-to-repo\dumdum (master -> origin)        
λ git checkout -b feature-branch                     
Switched to a new branch 'feature-branch'            
````
````                               
path-to-repo\dumdum (feature-branch -> origin)
λ git branch                                         
* feature-branch                                     
  master                                             
````
- git checkout branch-name : to switch to branch-name branch

- Pushing to branch
````
path-to-repo\dumdum (feature-branch -> origin)
λ git push
fatal: The current branch feature-branch has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature-branch
````

- I need to tell it which branch on GitHub I want to push to. --set-upstream flag has the shorthand -u.

````
path-to-repo\dumdum (feature-branch -> origin)
λ git push -u origin feature-branch
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 4 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (18/18), 2.41 KiB | 205.00 KiB/s, done.
Total 18 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), done.
remote:
remote: Create a pull request for 'feature-branch' on GitHub by visiting:

remote:      https://github.com/mahi397/dumdum/pull/new/feature-branch
remote:
To https://github.com/mahi397/dumdum.git
 * [new branch]      feature-branch -> feature-branch
Branch 'feature-branch' set up to track remote branch 'feature-branch' from 'origin'.
````

## Pull Request 
A request to have your code pulled into another branch.  
Say we want out code pulled from feature-branch into master branch, so we make a PR from the feature-branch to the master branch.  
Once we have made a PR, anyone can review our code, comment on it, ask us to make changes/updates.  
Once the PR is merged, you can delete your feature-branch.

- After merging PR from the feature-branch, checkout to master on local and "pull" the changes from origin to local master branch.
- git pull origin master would be used if upstream wasn't set. Since it is, we can just do git pull.
````
path-to-repo\dumdum (master -> origin)                            
λ git pull                                                               
remote: Enumerating objects: 13, done.                                   
remote: Counting objects: 100% (12/12), done.                            
remote: Compressing objects: 100% (7/7), done.                           
remote: Total 8 (delta 1), reused 0 (delta 0), pack-reused 0             
Unpacking objects: 100% (8/8), done.                                     
From https://github.com/mahi397/dumdum                                   
   edb2b75..06ec2dd  master         -> origin/master                     
   8f0583f..ffd71ab  feature-branch -> origin/feature-branch             
Updating edb2b75..06ec2dd                                                
Fast-forward                                                             
 Branching.md | 59 ++++++++++++++++++++++++++++++++++++++++++++++++++++++
+++++                                                                    
 Readme.md    | 14 +++++++-------                                        
 2 files changed, 66 insertions(+), 7 deletions(-)                       
 create mode 100644 Branching.md                                         
 ````
 
- Deleting a branch
````
path-to-repo\dumdum (master -> origin)
λ git branch -d feature-branch
Deleted branch feature-branch (was 8f0583f).
````
