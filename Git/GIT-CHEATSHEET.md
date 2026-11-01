# Git & GitHub Cheat Sheet

A practical reference guide covering Git fundamentals, configuration, core commands, synchronization, undoing changes, branches, history and GitHub workflows.

---

## 1. Git Fundamentals

| Keyword                   | Description                                                                   |
| ------------------------- | ----------------------------------------------------------------------------- |
| Git                       | Open-source distributed version control system used to track changes in code. |
| GitHub, GitLab, Bitbucket | Platforms for hosting and collaborating on Git repositories.                  |
| Staging                   | Area containing changes selected for the next commit.                         |
| Commit                    | Saves staged changes to the local repository.                                 |
| Branch                    | Independent line of development used to work on features separately.          |
| Clone                     | Creates a local copy of a remote repository, including its history.           |
| Remote                    | A reference to a repository hosted elsewhere, such as GitHub.                 |
| Fork                      | Personal copy of another user's repository.                                   |
| Pull Request              | A method of proposing changes to another branch or repository.                |
| HEAD                      | Reference to the currently checked-out commit.                                |

---

## 2. Git Configuration

| Command                                              | Description                          |
| ---------------------------------------------------- | ------------------------------------ |
| `git config --global user.name "Your Name"`          | Sets the author name for commits.    |
| `git config --global user.email "email@example.com"` | Sets the author email for commits.   |
| `git config --global color.ui true`                  | Enables colored command-line output. |
| `git config --list`                                  | Displays Git configuration settings. |

---

## 3. Core Git Commands

| Command                   | Description                                                       |
| ------------------------- | ----------------------------------------------------------------- |
| `git init`                | Initializes a new local repository.                               |
| `git clone <repo-url>`    | Clones a remote repository.                                       |
| `git add <file>`          | Stages a specific file.                                           |
| `git add <directory>`     | Stages a specific directory.                                      |
| `git add -A`              | Stages all changes, including additions and deletions.            |
| `git add .`               | Stages new and modified files in the current directory and below. |
| `git add -u`              | Stages modifications and deletions of tracked files.              |
| `git commit -m "message"` | Commits staged changes.                                           |
| `git status`              | Displays the current repository status.                           |

---

## 4. Synchronization of Changes

| Command                       | Description                                                   |
| ----------------------------- | ------------------------------------------------------------- |
| `git fetch`                   | Downloads updates from the remote repository without merging. |
| `git merge <branch>`          | Merges the specified branch into the current branch.          |
| `git pull`                    | Fetches and integrates changes from the remote branch.        |
| `git push`                    | Uploads local commits to the remote repository.               |
| `git remote -v`               | Displays configured remote repositories.                      |
| `git remote add origin <url>` | Adds a remote repository named origin.                        |

**Remember:** `git pull` generally performs a `git fetch` followed by integration (usually a merge, depending on configuration).

---

## 5. Undo Changes

| Command                     | Description                                                                       |
| --------------------------- | --------------------------------------------------------------------------------- |
| `git restore <file>`        | Discards unstaged changes in a file.                                              |
| `git revert <commit>`       | Creates a new commit that reverses a previous commit.                             |
| `git reset <file>`          | Removes a file from the staging area.                                             |
| `git reset --hard HEAD`     | Resets the working tree and staging area to the current commit.                   |
| `git reset --hard <commit>` | Resets the current branch to a specified commit and discards later local changes. |

**Warning:** `git reset --hard` permanently discards uncommitted changes. Use it carefully.

---

## 6. Branch Management

| Command                    | Description                                          |
| -------------------------- | ---------------------------------------------------- |
| `git branch <branch>`      | Creates a new branch.                                |
| `git checkout <branch>`    | Switches to an existing branch.                      |
| `git checkout -b <branch>` | Creates and switches to a new branch.                |
| `git switch <branch>`      | Switches branches.                                   |
| `git switch -c <branch>`   | Creates and switches to a new branch.                |
| `git merge <branch>`       | Merges the specified branch into the current branch. |
| `git branch -d <branch>`   | Deletes a merged local branch.                       |
| `git push origin <branch>` | Pushes a branch to the remote repository.            |
| `git branch`               | Lists local branches.                                |
| `git branch -r`            | Lists remote branches.                               |
| `git branch -a`            | Lists all local and remote branches.                 |

---

## 7. Git History

| Command                   | Description                              |
| ------------------------- | ---------------------------------------- |
| `git log`                 | Displays commit history.                 |
| `git log --author="name"` | Displays commits by a specific author.   |
| `git log --oneline`       | Displays compact commit history.         |
| `git show <commit>`       | Displays details of a particular commit. |
| `git blame <file>`        | Shows who modified each line and when.   |

---

## 8. Gitignore

A `.gitignore` file specifies files and directories that Git should ignore.

Create a `.gitignore` file in the root directory of your repository.

**Example:**

```gitignore
# Dependency directories
node_modules/

# Environment files
.env

# Log files
*.log

# Python cache
__pycache__/
*.pyc

# IDE settings
.vscode/

# System files
.DS_Store
```

**Important:** `.gitignore` does not automatically stop tracking files that Git already tracks.

Useful resources:

* [GitHub Gitignore Templates](https://github.com/github/gitignore)
* [Git Basics Cheatsheet](https://github.com/0nn0/git-basics-cheatsheet/blob/master/.gitignore)

---

## 9. Git Hosting Platforms

| Platform                            | Description                                                | Pricing             |
| ----------------------------------- | ---------------------------------------------------------- | ------------------- |
| [GitHub](https://github.com/)       | Popular platform for hosting Git repositories.             | Free and paid plans |
| [GitLab](https://gitlab.com/)       | Git hosting with integrated DevOps and CI/CD capabilities. | Free and paid plans |
| [Bitbucket](https://bitbucket.org/) | Git hosting platform with Atlassian integrations.          | Free and paid plans |

---

## 10. Git GUI Clients

| Client                                        | Operating System | Description                       |
| --------------------------------------------- | ---------------- | --------------------------------- |
| [GitHub Desktop](https://desktop.github.com/) | Windows, macOS   | Graphical Git client.             |
| [Sourcetree](https://www.sourcetreeapp.com/)  | Windows, macOS   | Visual Git repository management. |
| [Tower](https://www.git-tower.com/)           | Windows, macOS   | Advanced Git GUI client.          |

---

## 11. Useful Learning Resources

1. [Pro Git Book](https://git-scm.com/book/en/v2)
2. [Learn Git Concepts, Not Commands](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)
3. [Git Flight Rules](https://github.com/k88hudson/git-flight-rules)
4. [Git Flow](https://guides.github.com/introduction/flow/)
5. [GitHub Documentation](https://docs.github.com/)

---

## 12. Daily Git Workflow

These are the commands commonly used when working on a project:

```bash
# Check repository status
git status

# Stage changes
git add .

# Commit changes
git commit -m "Updated project files"

# Push changes to GitHub
git push origin main
```

**First-time repository setup:**

```bash
git init
git branch -M main
git remote add origin <repository-url>
git add .
git commit -m "Initial commit"
git push -u origin mainls
```

---

**Practice regularly:** Understanding Git commands and their workflow is an essential skill for DevOps, Cloud and Platform Engineering.
