# Git Conflict Lab
## Step 1 - Clone the project:
  - Clone the project ````git clone https://github.com/emsiemhong/git-conflict-lab.git````
## Step 2 - Create a branch to store your code
  - ````git checkout -b feature-1````
## Step 3 - Update code
  - In index.html file add your piece of code
  - ````
      <section id="feature-1">
        <h1>Feature 1</h1>
        <p>My name is Siemhong</p>
      </section>
    ````
## Step 4 - Update code in main branch
  - Your friend has been updated and merged code into main branch
  ### 1 - Checkout to main
    - Switch branch to main

    ````git checkout main````

    ***Note: You might ask to stash first before go to main

    ````git stash save feature-1````

  ### 2 - Pull code in main

    ````git pull origin main```

## Step 5 - Go back to your branch

  ````git checkout feature-1````

## Step 6 - Merge code from main to your branch

  ````git merge main````

  ***Note: If you have been stashed, you need to stash apply first
  ````git stash apply```` or ````git stash apply stash@{0}```
  If you want to review the stash ````git stash list````
## Step 7 - Fix conflict
  - <<<<<<< HEAD
  - ===========
  - >>>>>>> feature-1
  - ------------------------------------
  - You prefer #1 or #2 or both
  - 1. From <<<<<<<< HEAD to ==========
  - 2. From ======== to feature-1
## Step 8 - Resolve conflict
  - ````git add index.html````
  - ````git commit -m "Resolve conflict and add feature-1"````
## Step 9 - Push code, create pull request and merge
  - ````git push origin feature-1````
