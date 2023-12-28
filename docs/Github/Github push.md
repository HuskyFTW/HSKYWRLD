
# GitHub Push

This document provides a step-by-step guide on how to push changes to your GitHub repository.

## Steps

### 1. Make Changes to Your Files

Make the necessary changes to your files. This can include modifying existing files, adding new files, or deleting files.

### 2. Stage the Changes

Use the following command to stage the changes you've made. Staging prepares the changes for a commit.

```bash
git add .
```
This command adds all the changes in the current directory to the staging area. If you want to stage specific files, replace . with the file names.

### 3. Commit the Changes
Commit the staged changes with a descriptive message using the following command:

```bash
git commit -m "Describe the changes made in this commit"
```
### 4. Push the Changes to GitHub
Finally, push the committed changes to your GitHub repository using the following command:
```bash
git push -u origin
```

This command sends your committed changes to the remote repository on GitHub. If this is your first push or if you're pushing to a new branch, you might need to specify the branch name (e.g., git push origin main).

Now, your changes are reflected in your GitHub repository.