### Create a new repository on the command line

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

### Push an existing repository from the command line

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

### Update the changes to an existing repository from the command line

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
