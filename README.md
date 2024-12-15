# Version Control Systems

Version Control (also known as Version Management) refers to the process of tracking and managing changes to files or code over time. This helps ensure that we can:

- Keep track of changes across multiple files or a single file.
- Safely store and retrieve prior versions without consuming excessive storage space on your machine.

### Key Benefits of Version Control:

- **Backup and Restore**: Safeguard your work by saving periodic snapshots and easily reverting to previous versions.
- **Synchronization**: Ensure consistent and up-to-date files across multiple environments or team members.
- **Undo Changes**: Easily roll back any undesirable changes to a previous state.
- **Track Changes and Ownership**: Maintain a detailed history of changes, with clear ownership and authorship for each modification.
- **Sandboxing**: Work in isolated environments (branches) to experiment with new features or changes without affecting the main project.
- **Branching**: Create and manage multiple lines of development to work on features or fixes independently, without interfering with the main project.

### Version Control Types

#### Lock-Modify-Unlock Strategy

This strategy involves locking a file when it is being modified. The file can only be modified by one person at a time. Once the modification is complete, the file is unlocked for others to edit.
    
- **How it works**:
    - A user locks a file to make changes.
    - No one else can modify the file until it is unlocked by the original user.
    - Once the changes are finished, the file is unlocked, and others can modify it.
- **Pros**:
    - Prevents conflicting edits on the same file.
    - Simple and easy to manage.
- **Cons**:
    - Can lead to delays if files are locked for extended periods.
    - Not suitable for collaborative work where multiple people need to modify files simultaneously.

#### Copy-Modify-Merge Strategy

This strategy allows multiple users to make changes to the same file independently. After the changes are made, the modifications are merged into a single version.
    
- **How it works**:
    - Each user works on their own copy of the file.
    - Once the changes are made, the system attempts to automatically merge these changes into a single file.
    - If there are conflicting changes, the user is asked to resolve the conflicts manually.
- **Pros**:
    - Allows for more collaborative work, as multiple people can edit the same file simultaneously.
    - More flexible, as users do not need to lock files to make changes.
- **Cons**:
    - Merging conflicts can be time-consuming and complex.
    - Requires a robust merging tool or system to handle conflicts effectively.

#### Centralized vs. Distributed Version Control

Version Control Systems (VCS) can be divided into two main types based on their working mechanisms:

##### Centralized Version Control (CVCS)

In a Centralized Version Control System, there is a single central repository where all files and their version histories are stored. Users work on local copies of the files, but the main history and versioning are stored on the central server.

- Users check out a copy of the project from the central repository.
- They make changes locally and commit them back to the central repository.
- The central repository acts as the single source of truth for the project’s version history.
    
- **Examples**: Subversion (SVN), CVS
- **Pros**:
    - Centralized control allows for easy access and management of project history.
    - Simple to set up and use, especially for small teams.
    - Easier to enforce access control and permissions.
- **Cons**:
    - If the central repository is unavailable or corrupted, all users lose access to the project history.
    - Users cannot work offline; they need constant access to the central repository.
    - Can become a bottleneck in large teams or projects with frequent commits.

##### Distributed Version Control (DVCS)

In a Distributed Version Control System, each user has their own local repository, which includes the entire history of the project. Users can work independently and make commits without needing to be connected to a central server. Changes are later synchronized (pushed or pulled) between repositories.

- Each user clones the entire repository, which includes the full history and all versions.
- Users make changes and commit them to their local repository.
- Changes are shared with others through synchronization (e.g., using `git push` and `git pull` in Git).
- Merging occurs when changes from different users are combined.

- **Examples**: Git, Mercurial, Bazaar
    
- **Pros**:
    - Full project history is available locally, allowing for offline work and faster commits.
    - No single point of failure; each user’s repository is self-contained.
    - Ideal for collaborative work, as it allows easy branching, merging, and experimenting without affecting others’ work.
- **Cons**:
    - More complex setup and workflows, especially with larger teams.
    - Can lead to more complicated merge conflicts if changes are not synchronized properly.
    - Requires a more sophisticated system for handling large amounts of data and multiple branches.


# Text-based Computer Interaction

### Graphical User Interface (GUI)

- User-friendly
- Easy to explore and navigate

### Command Prompt

#### Windows Command Prompt

- Freeform commands
- Provides access to system directories, like the C drive

#### Pros:

- Time-saving
- Offers extensive capabilities such as:
    - Starting servers
    - Installing tools
    - Running code
    - Executing files
    - Working with Git

---
### Mac Terminology

- **Terminal**: The text input environment on Mac.
- **Shell**: The text input interface that handles commands.
- **Bash/Zsh (Z-Shell)**: Popular shells for executing commands on macOS.

--
### Common Terminal Commands:

- **`pwd`**: Print Working Directory (e.g., `/Users/melidiaz`) — shows the current location.
- **`ls`**: List Items — displays folders and files in the current directory.
- **`cd`**: Change Directory
    - `cd` (alone) — navigate to the home directory.
    - `cd ..` — move up one level in the directory.
    - `cd /` — navigate to the root directory.
    - `cd /Users` — go to the "Users" directory.
    - `cd + 'Tab'` — auto-complete or show directories with similar names.
- **`~`**: Represents the current user's home directory (e.g., `/Users/melidiaz`).

#### File and Directory Management:

- **`mkdir`**: Make Directory — creates a new folder.
- **`touch`**: Create a file — if the file doesn't exist, it creates a new one. If the file exists, it updates the timestamp.
- **`rm`**: Remove — deletes a file permanently.
- **`rmdir`**: Remove Directory — deletes an empty directory.
- **`rm -r`**: Remove Directory and Contents — recursively deletes a directory and its contents.

#### Additional Command Flags:

- **`-s`**: Shows file size.
- **`-l`**: Long format — displays detailed information about the files (e.g., permissions, size, modification date).

#### Man Pages (Manuals):

- **`man <command>`**: Displays the manual for a command (e.g., `man ls` for listing the options for `ls`).

#### Copy and Move Files:

- **`cp`**: Copy file(s) — `cp <source> <destination>`.
- **`cp -r`**: Copy directories and their contents recursively (e.g., `cp -r data/ copied/`).
- **`mv`**: Move or rename files/folders — `mv <source> <destination>`.

---

### Relative vs Absolute Paths

- **Relative Path**: Refers to the path starting from the current working directory to a target directory (e.g., `../Documents`).
- **Absolute Path**: The full path from the root directory to the target directory (e.g., `/Users/melidiaz/Documents`).

---
# GIT

Git is a free and open source version control system designed to handle everything form small to very large projects with speed and efficiency.

Git is about _control and tracking of code changes_ (or another stuff) over time. It’s a highly efficient version control tool.

**Git:**
- Version control system (is free and a local tool).
- Manage code history very efficiency.
- Track changes.

**GitHub:**
- The largest and most advance development platform in the world.
- Cloud hosting & collaboration provider.
- Git repository hosting.

## How Git Works

- Git tracks changes in a project using a **Git Repository**, which is hidden and represented by the `.git` folder.
- **Working Directory**: The local files you are working on.
- **Repository**: The storage area where the changes are tracked.

#### Repository Areas:

- **Staging Area (Index)**: A draft area where changes are prepared before committing.
- **Commits**: Snapshots of the project at specific points in time.

#### Key Concept:

Git **tracks changes** rather than storing entire files repeatedly. It compares new commits with previous ones, recording only the differences.

### Branches & Commits

#### **Working Directory/Tree**

- All the commits inside the working directory are stored in the **master branch** (e.g., commit 1, commit 2, commit 3...).

#### **Branches**

- Branches allow us to create an entire copy of the current state of the master branch.
- The project folder is not necessarily the **master branch**. We can work independently from the master branch and implement changes as needed.

##### **Workflow with Branches:**

1. Create a branch to work on a feature or change.
2. Once changes are complete, we can add the changes back to the master branch. This process is called a **merge**.
3. **Branches** are essentially subfolders within the Git project, providing a way to isolate work on separate tasks.

#### **Commits**

- A **commit** is essentially a 'snapshot' of the current state of the project at a specific point in time.

---
### Installing Git and First Steps

1. Install [Homebrew](https://brew.sh/index_es) 
2. Install Git:
    
    ```shell
    brew install git
    ```
    
3. Check if the installation was successful:
    
    ```shell
    git --version
    ```
    
4. For Visual Studio Code setup, refer to [Visual Studio Code Introduction](https://academind.com/tutorials/visual-studio-code-introduction).
    
5. Create a folder and open it in the IDE.
    
6. In the terminal of Visual Studio Code, initialize a Git repository:
    
    ```shell
    git status  # Check the working directory & staging area status
    git init    # Initialize the Git repository (first time)
    ```
    
> Use **Command + Shift + Period** to show hidden folders in Finder.

---
### Adding and Committing Files

1. To add a file to the staging area:
    
    ```shell
    git add <file>      # Add specific files
    git add .           # Add all files in the project folder
    ```
    
2. To commit changes:
    
    ```shell
    git commit -m "message"   # Commit with a message describing the change
    ```
    
3. To configure your Git credentials:
    
    ```shell
    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
    ```
    
    If you omit `--global`, your credentials will apply only to the current Git project.
    
4. To view all commits in the current branch:
    
    ```shell
    git log
    ```
    
    Example output:
    
    ```shell
    melidiaz@Melissas-MacBook-Air git-basics % git log
    commit 4f1a3e7202717fa29fb2f041882a11210c2c6177 (HEAD -> master)
    Author: melodiaz23 <meli.diaz23@gmail.com>
    Date:   Fri Jan 6 12:21:51 2023 -0500
    ```
    
5. To checkout a specific commit:
    
    ```shell
    git checkout <commit-id>    # Checkout a specific commit
    git checkout master         # Return to the master branch
    ```
    
### Working with Branches

- A **branch** represents a set of specific code changes.
- The **master branch** is the default name for the first branch in Git projects.

To see all the branches in your current project and check where you are:

```shell
git branch
```

To create a new branch:

```shell
git branch branch-name       # Create a new branch
git switch branch-name       # Switch to an existing branch
```

To switch to an existing branch:

```shell
git checkout branch-name     # Checkout an existing branch
```

To create and immediately switch to a new branch:

```shell
git checkout -b new-branch   # Create and checkout a new branch
```

If you create a new file in a branch, it exists only in that branch. To merge it into the master branch, use the following:

1. **Switch to master** before merging:
    
    ```shell
    git checkout master
    ```
    
2. **Merge the branch** into master:
    
    ```shell
    git merge branch-name
    ```    
> **Note**: Merging integrates changes from one branch into another.

### What is head?

Is the last commit and becautse we checkout the branch, is that specific branch wich idirectly points to the last commit in this branch.

> If we check a specific branch this branch holds differente commits and the latest commkit of a specific branch is then the so-called head.

### Detached HEAD

It is when a commit it's not related to a specific branch. -> A commit is in detached head state.

Explanation: [Using Git: What is a "Detached HEAD"?](https://www.youtube.com/watch?v=GN36mrrM12k)

### Branches and "git switch"

```sh
git switch
```

We used switch to create and check out a new branch -> It's related to working with branches.

And, to create a new branch:

```sh
git swicth -c [nameofthenewbranch]

```

### Deleting data

To check wich files are currently part of our staging area:

```sh
git ls-files
//List data in staging area

```

If we delate a file (already part of previous commit), we can use:

```sh
git rm <file name we are going to remove>
# run after file was delected fron working directory
# to also remove it from staging area
# or...
git add [file name we are going to add] 
# or .
# dot to add all working directory files to staging area

```

Once is deleted, we can commit the change.

To go back to the status of the latest commit (to undo a change, not stage for the commmit - unstaged changes):

```
git checkout [name of the file we want to refer to the head/latest commit]
//Or if we have some files and we want to go back to the head status of all commits on the currrent branch
git checkout . //go back to all

```

Another option, with a new command from Git is:

```
git restore [name of the file or dot .]

```

> Adding two dashes [--] tell Git that we don't refer to any specific branch, e.g: git checkout -- // revert changes in tracket files

If we have and untracked file we want to get rid of:

```
git clean -dn  // D for delete and We add n to list all the entries we'll to delete
// this help us to see what we're going to delete before...and then:
git clean -df // F stand for force. Force git to really do it without asking.

```

### Deleting Stage changes

Once we add the files to the stage area... if we want to undo that changes, we need to bring back the latest commit, tha latest stage of the file, and copy into the staging area:

```
git checkout [name of the file] and them:

git reset [name of the file]
// remove flie(s) from staging area
// Copy the latest committed change of a file into the staging area
//then we must to use checkout again.
git checkout [name of the file]

```

Another option is with **restore command**. It help us to restore and earlier stage of the project. In the case we want to restore the version prior:

```
git restore --staged [name of the file]
// Restore is more explicit than reset.
// Also remove file(s) from staging area
// and then
git checkout [name of the file]

```

### Latest commits

> Git reset helps us to reset the head of our branch (undo commits).

For example, to go back to the prior version of our last commit (_"delete"_ the last commit):

```
git reset --soft HEAD~1
//head because is the one that should be reset
// and ~1 according of the steps you want to go back.

```

With this, the commit is remove, the file is still in the working directory and in the staging area.

Another way is:

```
git reset HEAD~1 //The default way

```

That way, the file it will remove from the commit and the staging area. It will still remain on the working directory.

The hard way to reset the commits are:

```
git reset --hard HEAD~1

```

It will remove the commits, the files on the staging area and the file from the working directory.

### Branches

```
git branch
// To check the branches we have.

```

To delete branches we use -d or -D. Small d will only allow us to delete branches if we merge the branches already. Capital D, will force the deletion.

```
git branch -D <File to delete>
// -D force the deletion.
// or...
git branch -d <file to delete>

```

We can also delete multiple branches with one command, with one space between the name of the files.

```
git branch -D <file> <file>

```

> If we want to create a new branch:

```
git switch -c [name of the new branch]
// Witch -c it change of branch inmmediatly.

```

Change the name of the branch

```
git branch -m master main

```

## Git stash

Stash is like a internal memory, where we can save uncommitted unstaged changes.

```
git stash // To get back in our **latest** commit

git stash apply
// To get back to our unstage change.

git stash list // To get an overview of all our stash changes.
// stash@{0} is allways the latest.

git stash apply 1
// The number depends on what data stash we want to access.

```

If we access to some of this unstage data, we need to do something: stash it again, add the changes and commit these.

If we want, stash the changes, again:

```
git stash // In this case, with git stash, to come back
// now we will have a new file added to the working directory.

```

To add messages to our stashes:

```
git stash push m- "Message we want to let"
// m- for message.

```

To add one of the files to the project:

```
git stash pop 0
//The number depends on the index nunber we want to add to our project.
// This just means that we want to add this staged commit to our project
// and remove it from the stash.

```

We could also use git stash apply. With that, the data would still remain in the stash. With stash pop, the data is deleted from the stash and apply to the project.

To delete individual entries:

```
git stash drop 0
// Number according to the index number.

```

To clear the enter stash

```
git stash clear

```

## Git reflog

Help us if we if we deleted, a commit or a branch.

If we need to bring back a deleted information:

```
git reflog
//This give us an overview of all changes in this branch.
//It is a rolling back 30-day storage.

```

Then

```
git reset --hard 6944f15

```

reflog also help us with deleted branches.

```
git reflog
// Then, for branches...
git checkout 5f1e8ce
git switch -c feature
// create a new branch with the information of that branch.

```

## Combining master & feature branches

- **Master branch** is basically the main project branch that we have. And is the first branch we create in the project.
- **Feature branch** is a copy of the master branch where we can work on a new feature until it is complete.

### How combine master & feature branch?

### Merge types

- **Fast forward**: Only works if we have no additional commit in the master branch.

The fast forward merge moves the latest commits on feature to the HEAD. This action does not create new commit. Juts move.

```
git merge [nameofthebranchwewanttomerge]

```

To **undo the merge**: git reset --hard HEAD~2 //Number depends on the numbers of commit we want to go back.

Another way to do it, is with a so-called flag:

```
git merge --squash [nameofthebranchwewanttomerge]
//It will put together all the commits we had in our feature branch into the latest commit. Only one commit is added.
// With this we have to create a separate commit which contains all these changes.

```

- Non fast forward
    - **Recursive**
        
    - Octopus
        
    - Ours
        
    - Subtree
        
        git merge --no-ff [name of the branch] // Recursive strategy // We can also use this recursive merging strategy in cases where our fast-forward merge all the works.
        
        git tag
        

remove:

```
git tag -d [name of the tag]

```

adding a tag of the last commit

```
git tag -a [number of the version] -m '[message]' // Anotated tag

```

**rebase**

**merging conflict**

git merge --abort 
git log --merge 
git diff

**cherry-pick** git cherry-pick ['id commit']

**git tag**

- Lightwight tag
- Annoated tag

In git: git tag git tag 1.0 [id of the commit] git show [number of the tag]

## GitHub

### Remote Commands

```bash
git remote              # Show remote servers
git remote show origin  # Show detailed configuration
git ls-remote           # Check the remote repository
```

### Connecting Git with GitHub

```bash
git remote add origin [URL]  # Establish the connection between Git and GitHub
```

### Branches

To view branches:

```bash
git branch -a          # List local and remote tracking branches
git branch -r          # Show remote tracking branches
git branch             # Show local branches
git branch -vv         # More details about branches
```

To watch branches created on the remote repository:

```bash
git branch -a          # Show both local and remote branches
```

### Pushing and Pulling Data

To push or pull data:

```bash
git push origin master             # Push changes to the master branch
git pull origin master             # Pull changes from the master branch
git fetch origin master            # Fetch updates from the remote master branch
git push origin feature[name]      # Push a feature branch to the remote repository
```

To update the latest state without merging anything into your local structure:

```bash
git fetch origin                  # Fetch updates from the remote
git pull origin master             # Pull the latest changes from a specific branch
```

### Deleting Remote Branches

To delete a remote tracking branch:

```bash
git branch --delete --remotes origin/feature[name]  # Delete remote tracking branch locally
```

To delete a remote branch:

```bash
git push origin --delete feature[branch-name]  # Delete a remote branch
```

### Undoing Commits

To undo commits locally:

```bash
git reset --hard HEAD~1  # Delete the last commit locally
```

To update the remote branch after undoing:

```bash
git push origin master --force  # Force push to update the remote branch
```

---
### Branch Types

- **Local Branch**: A branch stored locally.
- **Remote Branch**: A branch stored on a remote repository.
- **Tracking Branch**: A branch that exchanges information between the local and remote repositories.
    - **Remote Tracking Branch**: Local copy of a remote branch (e.g., `git fetch`).
    - **Local Tracking Branch**: Local reference to a remote tracking branch (e.g., `git push`, `git pull`, `git fetch`).

### Creating a Local Tracking Branch

```bash
git branch --track feature-remote origin/feature-remote  # Create a local tracking branch
```

---
### Clone a Repository

```bash
git clone [URL]  # Clone a repository
```

### Upstream

```bash
git push -u origin feature-upstream  # The `-u` flag creates a local tracking branch
```

---

### Contributing to a Repository

1. Fork the repository.
2. Clone the repository on the local machine.
3. Make changes and create a commit.
4. Push the changes to the repository.
5. Create a pull request from the repository to the original repository.

## New Project Useful Commands

### Git Configuration

```bash
git config --global user.name "Name"   # Set Git username
git config --global user.email "name@example.com"  # Set Git email
```

- The `--global` flag applies these settings globally for all repositories in the system. If we omit `--global`, the settings will apply only to the current repository.

To check our current configuration:

```bash
git config --global --list   # List all global configurations
```

This ensures that the commits are properly attributed.

### Initializing a Repository

```bash
git init    # Initialize a new Git repository
git add .   # Add all files to the staging area
git commit -m 'message'  # Commit changes with a message
```

### Branching

```bash
git branch            # List all branches
git branch -m master main  # Rename the branch from 'master' to 'main'
git checkout -b [branch-name]  # Create and switch to a new branch
git branch -a         # List all local and remote branches
```

### Switching Branches

```bash
git checkout [branch-name]  # Switch to an existing branch
```

### Remote Operations

1. Create a repository on GitHub, then:

```bash
git remote add origin [URL]   # Add a remote repository URL
git push origin main           # Push the 'main' branch to the remote repository
git push origin [branch-name]  # Push a specific branch to the remote repository
```

2. To create a new branch and push changes:

```bash
git push --set-upstream origin [branch-name]  # Create the branch on remote and push
```

### Cloning a Repository

To clone an existing repository into the current directory (without creating a new folder):

```bash
git clone [URL] .  # Clone the repository into the current directory
```

### Pulling Changes

To fetch the latest changes from GitHub:

```bash
git pull                # Pull changes from the remote repository
git pull origin main    # Pull changes from the 'main' branch
```

### Merging Branches

To merge a branch into the `main` branch:

```bash
git merge [branch-name]  # Merge the specified branch into the current branch
```
