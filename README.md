# 💾 Git Repository Management Lab

## 💡 Project Overview

This repository demonstrates the fundamental workflow of Git for source code management. The steps cover initial repository setup, feature development using branching, integrating changes via merging, and synchronizing the work with a remote GitHub repository.

The primary goal was to apply essential Git commands to manage a project's history effectively.

## ⚙️ Key Git Operations Executed

The following core Git operations were successfully performed, demonstrating proficiency in the required workflow:

1.  **Repository Initialization and First Commit:**
    * `git init` was used to initialize the repository.
    * The first commit was created on the `master` (or `main`) branch, adding the initial file.
2.  **Branching and Feature Development:**
    * A dedicated **`feature-branch`** was created.
    * Work was performed and committed locally on this new branch.
3.  **Merging:**
    * The `feature-branch` was successfully **merged** back into the `master` branch using `git merge`.
4.  **Remote Synchronization:**
    * The local repository was connected to a remote GitHub repository.
    * All changes were pushed to the remote repository using `git push`.

This workflow meets the requirements of having at least two commits and a feature branch created and merged.

## 📜 Proof of Execution: Git Reflog

The `git reflog show --all` output provides irrefutable evidence of the entire command history, verifying the successful execution and sequencing of all required Git tasks (branching, commits, and merging).

The image below shows the chronological history of the repository's HEAD and branch pointers.

![Screenshot of the terminal showing the output of 'git reflog show --all', demonstrating the history of commits, branching, and merging.](/assets/Screenshot%20from%202025-12-10%2011-34-47.png)

### Key Events Confirmed in the Reflog:

* **Initial Commit (`7bbad44`):** Shows the "Initial commit: Added readme file" was created.
* **Branching:** Shows the `HEAD` moving from `master` to `feature-branch`, and the branch being created.
* **Feature Commit (`8bf35b7`):** Shows the new commit ("Updated readme with new feature text") created on the feature branch.
* **Merge:** Shows the `feature-branch` successfully merged into `master`.

## 🏃 Commands Used (Summary)

```bash
# 1. Initialization and First Commit
git init
echo "Hello Git!" > readme.txt
git add readme.txt
git commit -m "Initial commit: Added readme file"

# 2. Branching and Feature Work
git branch feature-branch
git checkout feature-branch
echo "New feature added!" >> readme.txt
git add readme.txt
git commit -m "Updated readme with new feature text"

# 3. Merge and Push
git checkout master
git merge feature-branch
git remote add origin <your-repo-link>
git push -u origin master