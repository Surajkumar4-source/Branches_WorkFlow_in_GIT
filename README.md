
# Creating and Merging Branches WorkFlow in GIT
<br>

## Step-by-Step Git Workflow

### 1. Initialize the Repository
- Start by creating a local Git repository:

    ```bash
    git init
    ```
*This initializes a new Git repository in your project directory, enabling Git to start tracking changes.*

### 2. Create and Edit Files
- Create and edit a file, then commit the changes:

```bash
    nano index.html
    git add .
    git commit -m "first commit"
```

- `nano index.html`: Opens `index.html` for editing.
- `git add .`: Stages all changes.
- `git commit -m "first commit"`: Commits the changes with a message.


### 3. Add Remote Repository
- Link your local repository to a remote repository:

```bash
    git remote add origin <link of your repo>
 

    Eg. in my case---    git remote add origin https://github.com/codeshare-ByRakesh/demo.git
```

*This command links your local repository to a GitHub repository.*

### 4. Create some more new files  and Commit  on `main`
- Create a file and push it to the remote repository:
```bash
    touch master.txt
    git add .
    git commit -m "first commit"
    git push origin main
```

- `git push origin main`: Pushes your local commits to the `main` branch on GitHub.

### 5. Create and Switch to a New Branch
Create a new branch and switch to it:

```bash
    git branch suraj
    git checkout suraj
```


- `git branch suraj`: Creates the `suraj` branch.
- `git checkout suraj`: Switches to the `suraj` branch.

### 6. Edit and Commit Changes on `suraj`
- On the `suraj` branch, create a file and commit it:
```bash
    nano filefromsuraj_branch.txt
    git add .
    git commit -m "2nd commit"
    git push origin suraj
```
- `git push origin suraj`: Pushes the `suraj` branch to GitHub.

### 7. Switch to `main` and Pull Changes
- Switch back to `main` and pull the latest changes:

```bash
  git checkout main
  git pull origin main
```
### 8. Merge `suraj` into `main`
Merge the `suraj` branch into `main`:

    git merge suraj

*If there are conflicts, Git will alert you to resolve them manually.*

### 9. Then again Commit and Push Merged Changes------ Final step
- After merging, commit and push the changes:
```bash
    git add .
    git commit -m "Merged suraj branch into main"
    git push origin main
```

### 10. Handle Push Rejection (if necessary)
- If the push is rejected, pull the latest changes and push again:
```bash
    git pull origin main
    git push origin main
```



<br>

- *Optional If you want to Delete a Branch*

```bash
   git branch <name of branch>
    git branch -d <name of branch>
```

- `git branch hello`: Creates a branch called `suraj`.  in my csae
- `git branch -d hello`: Deletes the `suraj` branch.    in my case



<br>
<br>
<br>

## Git Workflow Summary

### 1. Initialize Local Repository:

    git init
    git add .
    git commit -m "first commit"

### 2. Create Remote Repository:
   - Link remote: `git remote add origin <URL>`
   - Push initial commit: `git push origin main`

### 3. Create Feature Branch (`suraj`):
   - Create and switch: `git branch suraj && git checkout suraj`
   - Make changes, add, commit: `git commit -m "2nd commit"`
   - Push `suraj`: `git push origin suraj`

### 4. Merge `suraj` into `main`:
   - Switch to `main`: `git checkout main`
   - Pull latest: `git pull origin main`
   - Merge: `git merge suraj`
   - Push merged changes: `git push origin main`

### 5. Handle Push Rejection:
   - Pull remote changes: `git pull origin main`, then push.



<br>
<br>
<br>


### Key Concepts We’ve Learned:-
- *Branching: We created separate branches (main and suraj) to manage different features or work streams.*
- *Merging: We merged the suraj branch into main to integrate the changes.*
- *Collaboration: We pushed and pulled changes to collaborate with the remote repository (GitHub).*
- *Conflict Resolution: We can  resolved potential issues from diverging histories by pulling remote changes before pushing.*

  
### This is a standard Git workflow for managing feature branches and integrating them into a main or master branch while working with a remote repository.


