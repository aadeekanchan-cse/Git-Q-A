# Git Q&A

A simple collection of common Git questions and answers for quick reference.

## Questions & Answers

### 1. What is the difference between Git and GitHub?
**Git** is a distributed version control system that tracks changes in your files locally. **GitHub** is a cloud-based hosting platform for Git repositories that adds collaboration features like pull requests, issues, and CI/CD workflows.

### 2. How do I initialize a new Git repository?
Run the following command inside your project folder:
```bash
git init
```

### 3. What is the difference between `git add`, `git commit`, and `git push`?
- `git add <file>` (or `git add .`) stages changes for the next commit.
- `git commit -m "message"` saves the staged snapshot to your local repository history.
- `git push` uploads your local commits to a remote repository (such as GitHub).

### 4. How do I check the current status and history of my repository?
- Use `git status` to see modified, staged, and untracked files.
- Use `git log --oneline` to view a compact summary of recent commits.

### 5. What is the difference between `git pull` and `git fetch`?
- `git fetch` downloads new commits and branches from the remote repository without modifying your local working branch.
- `git pull` runs `git fetch` and immediately merges (or rebases) those remote changes into your current branch.

### 6. How do I create and switch to a new branch?
You can create and switch to a new branch in one step with:
```bash
git switch -c <branch-name>
```
*(Or using the older command: `git checkout -b <branch-name>`)*

### 7. What is the difference between `git merge` and `git rebase`?
- `git merge` combines two branches by creating a new merge commit, preserving the exact branching history.
- `git rebase` replays your branch's commits on top of another branch, creating a cleaner, linear history.

### 8. How do I undo uncommitted changes or save them temporarily?
- To temporarily save uncommitted changes without committing them, run `git stash` (and `git stash pop` to restore them later).
- To discard unstaged changes in a file, run `git restore <file>`.

### 9. How do I copy an existing remote repository to my machine?
Use `git clone <repository-url>` to download the full repository and its commit history into a new local directory:
```bash
git clone https://github.com/<username>/<repo>.git
```

### 10. How do I resolve a merge conflict?
When Git pauses a merge due to conflicting edits in the same lines:
1. Open the conflicted file(s) and look for `<<<<<<<`, `=======`, and `>>>>>>>` markers.
2. Edit the file to keep the desired code and remove all conflict markers.
3. Stage the resolved file and complete the merge:
```bash
git add <resolved-file>
git commit
```

