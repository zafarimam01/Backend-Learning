# Git Notes

## What is Git?

Git is a **Distributed Version Control System (DVCS)** used to track changes in source code, maintain project history, and collaborate with other developers.

### Advantages
- Tracks complete project history.
- Supports collaboration without overwriting others' work.
- Allows branching and merging.
- Enables rollback to previous versions.
- Works offline.

---

# Git vs GitHub

| Git | GitHub |
|-----|--------|
| Version Control System | Cloud platform for hosting Git repositories |
| Tracks source code history | Stores repositories online |
| Works locally | Enables collaboration, Pull Requests, Issues, Actions |

---

# Centralized vs Distributed Version Control

## Centralized Version Control (CVCS)

- Single central server stores project history.
- Developers depend on the server.
- Server failure can stop development.

Example:
- Apache Subversion (SVN)

---

## Distributed Version Control (DVCS)

- Every developer has a complete copy of the repository.
- Work can continue even without internet.
- Faster operations since most commands run locally.

Example:
- Git

---

# Git Workflow

```
Working Directory
        │
    git add
        ▼
 Staging Area
        │
 git commit
        ▼
 Local Repository
        │
   git push
        ▼
 Remote Repository (GitHub)
```

---

# Git Branch

A **branch** is a movable pointer to the latest commit.

Branches allow developers to work on features independently without affecting the main branch.

Benefits:

- Isolated development
- Easy experimentation
- Safe collaboration
- Clean project history

---

# Frequently Used Commands

## Repository

```bash
git init
git clone <url>
git status
git log --oneline
```

## Staging

```bash
git add .
git add <file>
git restore --staged <file>
```

## Commit

```bash
git commit -m "message"
```

## Branch

```bash
git branch
git switch <branch>
git switch -c feature-name
git merge feature-name
```

## Remote Repository

```bash
git remote -v
git push
git pull
git fetch
```

---

# Useful Commands

View changes

```bash
git diff
git diff --staged
```

Undo changes

```bash
git restore <file>
git reset --soft HEAD~1
git reset --hard HEAD~1
git revert <commit>
```

Temporary save

```bash
git stash
git stash pop
```

---

# Best Practices

- Commit frequently.
- Keep each commit focused on one logical change.
- Write meaningful commit messages.
- Pull before pushing changes.
- Review changes using `git diff`.
- Never commit passwords, API keys, or `.env` files.
- Use `.gitignore` from the beginning.
- Create separate branches for new features.

---

# Common Git Workflow

```bash
git pull origin main

git switch -c feature/new-feature

git add .

git commit -m "implement new feature"

git push -u origin feature/new-feature
```

---

# Important Files

## .gitignore

Specifies files and folders Git should ignore.

Examples:

- `.env`
- `.DS_Store`
- `node_modules/`
- `build/`

---

## .gitkeep

Git does not track empty directories.

A `.gitkeep` file is added to keep an empty folder inside the repository.

---

# Interview Questions

### What is Git?

A distributed version control system used to track source code changes.

### Difference between Git and GitHub?

Git is a version control tool.

GitHub is a cloud platform that hosts Git repositories.

### Difference between git fetch and git pull?

- `git fetch` downloads remote changes without merging.
- `git pull` downloads and merges remote changes.

### Difference between git reset and git revert?

- `git reset` rewrites history (use carefully).
- `git revert` creates a new commit that safely undoes changes.

### Why use branches?

To develop features independently without affecting the main branch.