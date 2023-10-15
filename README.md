## Create a new repository on the command line

1. **Initialize a Git repository in your project folder.**

```bash
git init
```

2. **Check the status of your files.**

```bash
git status
```

3. **Add files to the staging area.**

```bash
git add .
```

4. **Commit the changes.**

```bash
git commit -m "first commit"
```

5. **Rename the default branch (if desired).**

```bash
git branch -M main
```

6. **Link your local repository to your GitHub repository.**

```bash
git remote add origin <YOUR_GITHUB_REPO_LINK>
```

7. **Push the commits to GitHub.**

```bash
git push -u origin main
```

---

## Push an existing repository from the command line

1. **If no GitHub repo is linked, add it first:**

```bash
git remote add origin <YOUR_GITHUB_REPO_LINK>
```

2. **Rename the default branch (if desired).**

```bash
git branch -M main
```

3. **Add and commit your changes:**

```bash
git add .
```

```bash
git commit -m "updated commit name"
```

4. **Push to GitHub:**

```bash
git push -u origin main
```

---

## Update the changes to an existing repository from the command line

1. **Add and commit your changes:**

```bash
git add .
```

```bash
git commit -m "updated commit name"
```

2. **Push to GitHub:**

```bash
git push
```

---

## Stashing Changes

Sometimes, you may be in the middle of working on something when you need to switch contexts (e.g., to work on another task). Stashing allows you to save these changes without committing them.

1. **Stash your changes**:

```bash
git stash save "Description of changes you're stashing"
```

(The description is optional but helps if you have multiple stashes.)

2. **List all stashes**:

```bash
git stash list
```

3. **Apply a stash and keep it in stash list**:

```bash
git stash apply stash@{n} # Replace n with the stash number you want to apply.
```

4. **Apply the latest stash and remove it from stash list**:

```bash
git stash pop
```

5. **Delete a stash**:

```bash
git stash drop stash@{n} # Replace n with the stash number you want to delete.
```

6. **Clear all stashes**:

```bash
git stash clear
```

## Branching

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

When you want to delete a branch, the `-d` option will prevent deletion if the branch contains changes that are not yet merged. Sometimes, you may want to forcefully delete a branch regardless of these changes. This is where the `-D` option comes in.

5. **Force delete a local branch**:

```bash
git branch -D branch_name
```

6. **Delete a remote branch**:

```bash
git push origin --delete branch_name
```

**Caution**: Using `-D` to forcefully delete a branch will discard all the commits in that branch which haven't been merged. Always double-check before using this command to ensure you don't lose any important changes.

## Merging

1. **Merge another branch into your active branch**:

```bash
git merge branch_name
```

(Before doing the merge, you should be in the branch you want to merge into. For example, if you want to merge `feature` branch into `main`, first checkout `main` and then execute the merge command.)

2. **If there are merge conflicts, you'll need to resolve them**. Once you've resolved them:

```bash
git add . # to stage the resolved conflicts
```

```bash
git commit
```

3. **If you want to abort a merge (maybe because of conflicts you can't resolve)**:

```bash
git merge --abort
```

## Other Useful Commands

1. **View commit logs**:

```bash
git log
```

2. **View short commit logs**:

```bash
git log --oneline
```

3. **Undo the last commit (without losing changes)**:

```bash
git reset HEAD~1
```

4. **View commit logs with a graph**:

```bash
git log --graph
```

To make it even more useful, you can combine `--graph` with other `git log` options. A common combination is:

```bash
git log --graph --oneline --all
```

- `--oneline` condenses each commit to a single line which makes it easier to browse through when combined with the graph.
- `--all` shows all references (i.e., all branches, tags, etc.).
