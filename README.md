## Git Command-Line Essentials

---

## Git Configuration

1. **Checking the git configuration**:

   ```bash
   git config --list
   ```

2. **Setting global username and email**:

   ```bash
   git config --global user.name "Your Name"
   ```

   ```bash
   git config --global user.email "your.email@example.com"
   ```

---

## Create a New Repository on the Command Line

1. **Initialize a Git repository in your project folder**:

   ```bash
   git init
   ```

2. **Check the status of your files**:

   ```bash
   git status
   ```

3. **Add files to the staging area**:

   ```bash
   git add .
   ```

4. **Commit the changes**:

   ```bash
   git commit -m "first commit"
   ```

5. **Rename the default branch (if desired)**:

   ```bash
   git branch -M main
   ```

6. **Link your local repository to your GitHub repository**:

   ```bash
   git remote add origin <YOUR_GITHUB_REPO_LINK>
   ```

7. **Push the commits to GitHub**:
   ```bash
   git push -u origin main
   ```
   **Note**: If you are pushing to GitHub for the first time or from a new device, you will be prompted to log in to your GitHub account. Depending on your setup, you may use a username and password, a personal access token, or SSH key authentication.

---

## Cloning and Updating Repositories

1. **Cloning a repository**:

   ```bash
   git clone <REPO_LINK>
   ```

2. **Fetching updates from a remote without merging**:

   ```bash
   git fetch origin
   ```

3. **Pulling updates from a remote**:
   ```bash
   git pull origin main
   ```

---

## Working with Branches

1. **List all branches**:

   ```bash
   git branch
   ```

2. **Create a new branch**:

   ```bash
   git branch branch_name
   ```

3. **Switch to a branch**:

   ```bash
   git checkout branch_name
   ```

   Or, create and switch to a new branch in one command:

   ```bash
   git checkout -b branch_name
   ```

4. **Delete a branch**:

   ```bash
   git branch -d branch_name
   ```

5. **Force delete a local branch**:
   ```bash
   git branch -D branch_name
   ```

---

## Merging and Handling Conflicts

1. **Merge another branch into your active branch**:

   ```bash
   git merge branch_name
   ```

2. **If there are merge conflicts, resolve them and then**:

   ```bash
   git add . # to stage the resolved conflicts
   ```

   ```bash
   git commit
   ```

3. **Abort a merge (due to unresolved conflicts)**:
   ```bash
   git merge --abort
   ```

---

## Listing Merged and Unmerged Branches:

When working with multiple branches, it can be useful to know which branches have already been merged into the current branch and which have not. This helps in managing branches, cleaning up merged branches, and avoiding redundant work.

1. **List branches that have been merged**:

   ```bash
   git branch --merged
   ```

2. **List branches that have NOT been merged**:

   ```bash
   git branch --no-merged
   ```

3. **Shows all branches (local and remote) that have been merged into the current branch**:

   ```bash
   git branch -a --merged
   ```

---

## Stashing Changes

1. **Stash your changes**:

   ```bash
   git stash save "Description of changes you're stashing"
   ```

2. **List all stashes**:

   ```bash
   git stash list
   ```

3. **Apply a stash**:

   ```bash
   git stash apply stash@{n}
   ```

4. **Delete a stash**:

   ```bash
   git stash drop stash@{n}
   ```

5. **Clear all stashes**:
   ```bash
   git stash clear
   ```

---

## Viewing Commit History and Differences

1. **View commit logs**:

   ```bash
   git log
   ```

2. **View short commit logs**:

   ```bash
   git log --oneline
   ```

3. **View commit logs with a graph**:

   ```bash
   git log --graph
   ```

   With additional options:

   ```bash
   git log --graph --oneline --all
   ```

4. **Viewing differences between branches**:
   ```bash
   git diff main..your_branch_name
   ```

---

## Miscellaneous Commands

1. **Undo the last commit (without losing changes)**:

   ```bash
   git reset HEAD~1
   ```

2. **Viewing remote repositories linked to your local repo**:
   ```bash
   git remote -v
   ```

---
