# 🚀 Git & GitHub – Complete Learning Roadmap

> A complete beginner-to-professional learning guide covering 12 sections, practical commands, real-time workflows, and interview preparation.

## 🎯 Learning Objectives

- Understand Git and GitHub from basics to advanced.
- Learn all important Git commands with practical examples.
- Understand Git architecture and internal workflow.
- Work with branches, merging, rebasing, and conflicts.
- Learn professional team collaboration workflows.
- Practice real-time company scenarios.
- Prepare for Git and GitHub technical interviews.

---

## 📚 Complete Syllabus – 12 Sections

| Section | Topic | Status |
|---|---|---|
| 01 | Introduction to Version Control | ⬜ Pending |
| 02 | Installing and Configuring Git | ⬜ Pending |
| 03 | Git Architecture | ⬜ Pending |
| 04 | Basic Git Commands | ⬜ Pending |
| 05 | Working with Remote Repositories | ⬜ Pending |
| 06 | Branching | ⬜ Pending |
| 07 | Enterprise Branching Strategies | ⬜ Pending |
| 08 | Merge and Rebase | ⬜ Pending |
| 09 | Merge Conflicts | ⬜ Pending |
| 10 | Pull Requests and Code Review | ⬜ Pending |
| 11 | Undoing Changes | ⬜ Pending |
| 12 | Other Important Git Commands | ⬜ Pending |

---

# Section 01 – Introduction to Version Control

### Topics

- What is Version Control?
- Why do software development teams need Version Control?
- Problems without Version Control.
- Types of Version Control Systems:
  - Local Version Control System
  - Centralized Version Control System (SVN)
  - Distributed Version Control System (Git)
- What is Git?
- History of Git.
- What is GitHub?
- Difference between Git and GitHub.
- Git vs GitHub vs GitLab vs Bitbucket.
- Important Git terminology:
  - Repository
  - Commit
  - Branch
  - Remote
  - Clone

### Practical Learning

- Understand version control with real-time examples.
- Compare Local, Centralized, and Distributed systems.
- Understand how developers collaborate using Git.

---

# Section 02 – Installing and Configuring Git

### Topics

- Installing Git on Windows.
- Understanding Git Bash, CMD, and PowerShell.
- Verifying Git installation.
- Understanding Git configuration.
- System-level configuration.
- Global-level configuration.
- Local-level configuration.
- Configuration priority.
- Setting username and email.
- Configuring the default branch.
- Viewing Git configuration.
- Understanding SSH authentication.
- Generating SSH keys.
- Adding SSH public keys to GitHub.
- Testing SSH connection.
- Difference between HTTPS and SSH.

### Important Commands

```bash
git --version

git config --system --list
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

git config --local user.name "Your Name"
git config --local user.email "your-email@example.com"

git config --list
git config --show-origin --list

git config --global init.defaultBranch main

ssh-keygen -t ed25519 -C "your-email@example.com"

ssh -T git@github.com
```

---

# Section 03 – Git Architecture

### Topics

- Understanding Git Architecture.
- Working Directory.
- Staging Area (Index).
- Local Repository.
- Git workflow.
- Understanding file lifecycle.
- Untracked files.
- Tracked files.
- Modified files.
- Staged files.
- Committed files.
- Understanding the `.git` directory.
- Git objects:
  - Blob
  - Tree
  - Commit
  - Tag
- Understanding SHA hashes.
- Understanding HEAD.
- Branch references.
- Detached HEAD state.
- Git snapshot mechanism.

### Important Commands

```bash
git status
git add filename
git commit -m "message"
git log
git show
ls -la
cat .git/HEAD
```

### Git Architecture Diagram

```text
        Working Directory
                |
                | git add
                v
          Staging Area
                |
                | git commit
                v
         Local Repository
                |
                | git push
                v
        Remote Repository
             (GitHub)
```

---

# Section 04 – Basic Git Commands

### Topics

- Creating a Git repository.
- Initializing a repository.
- Cloning an existing repository.
- Checking repository status.
- Adding files to staging area.
- Committing changes.
- Viewing commit history.
- Comparing file changes.
- Removing files.
- Renaming and moving files.
- Unstaging files.
- Discarding local changes.
- Amending the latest commit.

### Important Commands

```bash
git init

git clone <repository-url>

git status
git status -s

git add filename
git add .
git add -A

git commit -m "Initial commit"

git log
git log --oneline
git log --graph --oneline --all

git diff
git diff --staged

git rm filename
git rm --cached filename

git mv oldname newname

git restore filename
git restore --staged filename

git commit --amend
```

### Practical Tasks

- Create a new repository.
- Create HTML, CSS, and Java files.
- Add files to staging.
- Commit changes.
- Modify existing files.
- Compare changes using `git diff`.
- Remove and restore files.
- View commit history.

---

# Section 05 – Working with Remote Repositories

### Topics

- What is a Remote Repository?
- Local Repository vs Remote Repository.
- Understanding GitHub repositories.
- Connecting local repository to GitHub.
- Understanding `origin`.
- Adding and removing remote URLs.
- Pushing local commits to GitHub.
- Fetching remote changes.
- Pulling remote changes.
- Understanding upstream branches.
- Tracking branches.
- Ahead and behind commits.
- Difference between `git fetch` and `git pull`.

### Important Commands

```bash
git remote
git remote -v

git remote add origin <repository-url>

git remote remove origin

git push origin main
git push -u origin main

git fetch origin

git pull origin main

git branch -vv

git log main..origin/main --oneline
```

### Practical Tasks

- Create a GitHub repository.
- Connect a local repository to GitHub.
- Push code to GitHub.
- Modify files directly on GitHub.
- Fetch remote changes.
- Pull remote changes into local repository.

---

# Section 06 – Branching

### Topics

- What is a Branch?
- Why do developers use branches?
- Understanding branch pointers.
- HEAD and branch movement.
- Creating branches.
- Switching branches.
- Creating and switching branches together.
- Listing local and remote branches.
- Renaming branches.
- Deleting branches.
- Detached HEAD state.
- Local branches vs Remote-tracking branches.
- Branch tracking.

### Important Commands

```bash
git branch

git branch feature/login

git switch feature/login

git switch -c feature/register

git branch -a
git branch -r
git branch -vv

git branch -m old-name new-name

git branch -d feature/login
git branch -D feature/login

git push origin --delete feature/login
```

### Practical Tasks

- Create a main branch.
- Create login and register feature branches.
- Work independently in different branches.
- Switch between branches.
- Merge completed feature branches.
- Delete unnecessary branches.

---

# Section 07 – Enterprise Branching Strategies

### Topics

- What is a Branching Strategy?
- Why companies follow branching strategies?
- Gitflow Workflow.
- Feature Branch Workflow.
- Trunk-Based Development.
- Understanding main branch.
- Understanding develop branch.
- Feature branches.
- Release branches.
- Hotfix branches.
- Branch naming conventions.
- Protected branches.
- Branch permissions.
- Code review requirements.

### Gitflow Structure

```text
main
  |
  |-------------------------|
  |                         |
develop                  hotfix
  |                         |
  |                       main
  |
feature/login
feature/register
  |
release/v1.0
  |
main
```

### Practical Tasks

- Create feature branches.
- Implement features independently.
- Create release branches.
- Understand hotfix workflow.
- Practice a professional team workflow.

---

# Section 08 – Merge and Rebase

### Topics

- What is Git Merge?
- Why do we merge branches?
- Fast-forward merge.
- Three-way merge.
- Non-fast-forward merge.
- Merge commits.
- Understanding common ancestors.
- What is Git Rebase?
- How rebase works internally.
- Merge vs Rebase.
- Interactive Rebase.
- Squash commits.
- Rebase conflict resolution.
- Best practices for merge and rebase.

### Important Commands

```bash
git merge feature/login

git merge --ff-only feature/login

git merge --no-ff feature/login

git rebase main

git rebase -i HEAD~3

git rebase --continue

git rebase --abort

git merge --abort

git merge --squash feature/login
```

### Practical Tasks

- Merge feature branches into main.
- Practice fast-forward merging.
- Practice three-way merging.
- Rebase a feature branch.
- Resolve rebase conflicts.
- Squash multiple commits.

---

# Section 09 – Merge Conflicts

### Topics

- What is a Merge Conflict?
- Why do merge conflicts happen?
- Common conflict scenarios.
- Understanding conflict markers.
- Identifying conflicted files.
- Resolving conflicts manually.
- Resolving conflicts using VS Code.
- Accept Current Change.
- Accept Incoming Change.
- Accept Both Changes.
- Completing a merge after conflict resolution.
- Aborting a merge.
- Preventing merge conflicts.

### Conflict Markers

```text
<<<<<<< HEAD
Your current branch changes
=======
Incoming branch changes
>>>>>>> feature/login
```

### Important Commands

```bash
git status

git diff --name-only --diff-filter=U

git add filename

git commit

git merge --abort
```

### Practical Tasks

- Create two branches.
- Modify the same line in both branches.
- Merge the branches.
- Generate a merge conflict.
- Resolve the conflict.
- Complete the merge.
- Verify the final code.

---

# Section 10 – Pull Requests and Code Review

### Topics

- What is a Pull Request (PR)?
- Why do companies use Pull Requests?
- Pull Request vs Git Merge.
- Base branch and Compare branch.
- Creating a Pull Request on GitHub.
- Adding reviewers.
- Assigning team members.
- Writing PR descriptions.
- Reviewing code.
- Approving Pull Requests.
- Requesting changes.
- Resolving review comments.
- Draft Pull Requests.
- PR merge strategies:
  - Merge Commit
  - Squash and Merge
  - Rebase and Merge
- Closing Pull Requests.
- Deleting merged branches.

### Professional Workflow

```text
main
 |
 | Create feature branch
 v
feature/login
 |
 | Write code
 | Commit changes
 | Push branch
 v
GitHub Repository
 |
 | Create Pull Request
 v
Code Review
 |
 | Approval
 v
Merge into main
 |
 v
Delete Feature Branch
```

### Important Commands

```bash
git switch main

git pull origin main

git switch -c feature/login

git add .
git commit -m "Add login feature"

git push -u origin feature/login

git branch -d feature/login

git push origin --delete feature/login
```

---

# Section 11 – Undoing Changes

### Topics

- Why do developers undo changes?
- Discarding working directory changes.
- Unstaging files.
- Understanding Git Restore.
- Understanding Git Reset.
- Soft Reset.
- Mixed Reset.
- Hard Reset.
- Understanding Git Revert.
- Difference between Reset and Revert.
- Recovering deleted commits.
- Understanding Git Reflog.
- Recovering previous branch states.

### Important Commands

```bash
git restore filename

git restore --staged filename

git reset --soft HEAD~1

git reset --mixed HEAD~1

git reset --hard HEAD~1

git revert <commit-id>

git revert --continue

git revert --abort

git reflog
```

### Important Difference

| Command | Purpose |
|---|---|
| `git restore` | Discard or restore file changes |
| `git reset` | Move branch pointer and adjust staging/worktree |
| `git revert` | Create a new commit that reverses another commit |
| `git reflog` | View local reference movement history |

### Practical Tasks

- Modify and restore files.
- Unstage files.
- Undo the latest local commit.
- Revert a pushed commit safely.
- Recover a previous commit using reflog.

---

# Section 12 – Other Important Git Commands

### 1. Git Stash

Temporarily saves unfinished changes without creating a commit.

```bash
git stash

git stash push -m "Work in progress"

git stash -u

git stash list

git stash pop

git stash apply

git stash drop stash@{0}

git stash clear
```

### 2. Git Cherry-Pick

Apply a specific commit from another branch to the current branch.

```bash
git cherry-pick <commit-id>

git cherry-pick --continue

git cherry-pick --abort
```

### 3. Git Tags

Used to mark important points in repository history, such as software releases.

```bash
git tag

git tag v1.0.0

git tag -a v1.0.0 -m "First release"

git show v1.0.0

git push origin v1.0.0

git push origin --tags

git tag -d v1.0.0

git push origin --delete v1.0.0
```

### 4. Git Ignore

Prevents specified untracked files from being added to Git.

Example `.gitignore`:

```gitignore
*.class
target/
node_modules/
.idea/
.vscode/
.env
application-local.properties
```

Important commands:

```bash
git check-ignore -v filename

git status --ignored

git rm --cached filename
```

### 5. Git Cherry-Pick, Stash and Tags – Practical Tasks

- Save unfinished work using stash.
- Restore stashed changes.
- Apply a specific commit using cherry-pick.
- Create release tags.
- Push tags to GitHub.
- Configure `.gitignore`.

### 6. Security Best Practices

- Never commit passwords.
- Never upload API keys or access tokens.
- Never share private SSH keys.
- Use environment variables for secrets.
- Use `.gitignore` for local configuration files.
- If a secret is exposed, revoke or rotate it immediately.
- Remember: `.gitignore` does not remove secrets already committed.

---

# 🏢 Real-Time Company Workflow

Understand and practice this complete workflow:

```text
Developer receives a task
          |
          v
Pull latest main branch
          |
          v
Create feature branch
          |
          v
Write application code
          |
          v
Test the application
          |
          v
Stage and commit changes
          |
          v
Push feature branch
          |
          v
Create Pull Request
          |
          v
Code Review
          |
          v
Resolve review comments
          |
          v
PR Approval
          |
          v
Merge into main
          |
          v
Deploy application
```

---

# 💻 Final Practical Project

## Employee Management System

Build a Java-based Employee Management System and use Git/GitHub to manage the complete development process.

### Features

- Employee Registration
- View Employee Details
- Update Employee Details
- Delete Employee Details
- Employee Search
- Login System

### Git Practice

- Create a GitHub repository.
- Initialize a local repository.
- Create a main branch.
- Create feature branches.
- Develop individual features.
- Commit changes regularly.
- Push code to GitHub.
- Create Pull Requests.
- Review code.
- Resolve merge conflicts.
- Merge completed features.
- Create a release tag.

---

# 🎤 Git & GitHub Interview Preparation

Prepare answers for these questions:

1. What is Git?
2. What is GitHub?
3. Difference between Git and GitHub?
4. What is Version Control?
5. What is a Distributed Version Control System?
6. What is a Git repository?
7. What is the difference between `git init` and `git clone`?
8. What is the difference between `git add` and `git commit`?
9. What is the staging area?
10. What is the difference between global and local configuration?
11. What is the `.git` folder?
12. What is HEAD in Git?
13. What is a branch?
14. What is the difference between merge and rebase?
15. What is a fast-forward merge?
16. What is a merge conflict?
17. How do you resolve a merge conflict?
18. What is a remote repository?
19. What is the difference between fetch and pull?
20. What is the difference between push and pull?
21. What is a Pull Request?
22. What is code review?
23. What is Git stash?
24. What is Git cherry-pick?
25. What is Git revert?
26. What is Git reset?
27. What is the difference between reset and revert?
28. What is Git reflog?
29. What is `.gitignore`?
30. What is a Git tag?
31. What is Gitflow?
32. What is a protected branch?
33. What is detached HEAD?
34. What is SSH authentication?
35. How do developers use Git in real-time projects?

---

# 📖 Learning Resources

- [Official Git Website](https://git-scm.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [Official Git Documentation](https://git-scm.com/docs)
- [GitHub Documentation](https://docs.github.com/)

---

# ✅ Final Completion Checklist

- [ ] Understand all 12 sections.
- [ ] Practice every important Git command.
- [ ] Understand Git architecture.
- [ ] Create and manage repositories.
- [ ] Work with local and remote branches.
- [ ] Practice merge and rebase.
- [ ] Resolve merge conflicts.
- [ ] Create and review Pull Requests.
- [ ] Understand undo and recovery commands.
- [ ] Complete the Employee Management System Git workflow.
- [ ] Prepare interview questions and answers.
- [ ] Explain Git workflow confidently to a manager.

---

## 🏆 Final Goal

**Become confident in using Git and GitHub in a real-time software development environment.**

Learn the concepts, understand the commands, practice independently, and explain every workflow clearly.

**Don't just memorize commands. Understand how and why they work.**