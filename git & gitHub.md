# **Git - 0 to Pro Reference** 🚀  
**By: SuperSimple.dev**  
**Tutorial Link:** [Git - 0 to Pro](https://www.youtube.com/watch?v=hrTQipWp6co)  

---

## **Command Line Basics** 💻  
### **Common Commands**  
| Command               | Description                                      |  
|-----------------------|--------------------------------------------------|  
| `ls`                  | List files and folders in the current directory. |  
| `cd ~/Desktop/folder` | Change the directory to the specified folder.    |  

**Note:** Git commands must be run inside the folder containing your code.  

---

## **Creating Commits** 📝  
### **Key Concepts**  
- **Version = Commit**  
- **Version History = Commit History**  

### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git init`                       | Start tracking changes in the current folder.    |  
| `git status`                     | Show changes since the last commit.              |  
| `git add <file|folder>`          | Add changes to the staging area.                |  
| `git add file`                   | Add a specific file.                            |  
| `git add folder/`                | Add all files in a folder (and subfolders).     |  
| `git add .`                      | Add all files in the current directory.         |  
| `git commit -m "message"`        | Create a commit with a message.                 |  
| `git commit -m "message" --amend`| Update the previous commit.                     |  
| `git log`                        | View commit history.                            |  
| `git log --all`                  | Show all commits (not just the current branch). |  
| `git log --all --graph`          | Show branching visually.                        |  

---

## **Configure Name & Email** 📧  
```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

---

## **Working Area vs. Staging Area** 🔄  
- **Working Area:** Contains changes that start here.  
- **Staging Area:** Contains changes that will go into the next commit.  

### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git add .`                      | Move changes from working to staging.           |  
| `git commit -m "message"`        | Move changes from staging to commit history.    |  
| `git reset <file|folder>`        | Move changes from staging back to working.      |  
| `git reset file`                 | Reset a specific file.                          |  
| `git reset folder/`              | Reset all files in a folder.                    |  
| `git reset .`                    | Reset all files in the current directory.       |  
| `git checkout -- <file|folder>`  | Discard changes in the working area.            |  
| `git checkout -- file`           | Discard changes for a specific file.            |  
| `git checkout -- folder/`        | Discard changes for all files in a folder.      |  
| `git checkout -- .`              | Discard all changes in the working area.        |  

---

## **Viewing & Restoring Previous Commits** ⏮️  
### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git checkout <commit_hash>`     | View a previous commit.                         |  
| `git checkout <hash|branch> file`| Restore a file to a previous commit.            |  
| `git checkout <hash|branch> folder/` | Restore all files in a folder.              |  
| `git checkout <hash|branch> .`   | Restore all files in the project.               |  

---

## **Other Git Features** 🛠️  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git config --global alias.shortcut <command>` | Create a shortcut.         |  
| `git config --global alias.s "status"`         | Example: `git s` = `git status`. |  
| `.gitignore`                     | Tell Git which files/folders to ignore.          |  
| `rm -rf .git`                    | Remove Git from the project.                    |  

---

## **GitHub Basics** 🌐  
### **Key Concepts**  
- **Repository:** A folder containing code tracked by Git.  
- **GitHub:** A service to save Git repositories online.  
  - Backup code.  
  - View history easily.  
  - Alternatives: Bitbucket, GitLab.  
- **Local Repository:** Saved on your computer.  
- **Remote Repository:** Saved online (e.g., GitHub).  

---

## **Uploading Code to GitHub** ⬆️  
### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git remote add <remote_name> <url>` | Link local repository to remote repository. |  
| `git remote add origin <url>`    | Example: Link to GitHub repository.             |  
| `git remote`                     | List all linked remote repositories.            |  
| `git remote -v`                  | List remote repositories with details.          |  
| `git remote remove <remote_name>`| Remove a remote repository link.                |  
| `git config --global credential.username <username>` | Configure GitHub username. |  
| `git push <remote_name> <branch>`| Upload a branch to the remote repository.       |  
| `git push origin main`           | Example: Upload the `main` branch.              |  
| `git push origin main --set-upstream` | Set up a shortcut for future pushes.   |  
| `git push <remote_name> <branch> -f` | Force-push (overwrite remote repository). |  

---

## **Downloading Code from GitHub** ⬇️  
### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git clone <url>`                | Download a remote repository.                   |  
| `git clone <url> <folder_name>`  | Download and rename the folder.                 |  
| `git fetch`                      | Update remote tracking branches.                |  
| `git pull <remote_name> <branch>`| Update local branch with remote changes.        |  
| `git pull origin main`           | Example: Update `main` branch.                  |  
| `git pull origin main --set-upstream` | Set up a shortcut for future pulls.     |  

---

## **Branching** 🌿  
### **Key Concepts**  
- **Branching:** Create a copy of the version history to work on without affecting the original.  

### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git branch <branch_name>`       | Create a new branch.                            |  
| `git branch feature1`            | Example: Create `feature1` branch.              |  
| `git checkout <branch_name>`     | Switch to a branch.                             |  
| `git checkout feature1`          | Example: Switch to `feature1` branch.           |  
| `git branch -D <branch_name>`    | Delete a branch.                                |  
| `git branch -D feature1`         | Example: Delete `feature1` branch.              |  

---

## **Merging** 🔀  
### **Commands**  
| Command                          | Description                                      |  
|----------------------------------|--------------------------------------------------|  
| `git merge <branch_name> -m "message"` | Merge a branch into the current branch. |  
| `git checkout main`              | Switch to `main` branch.                        |  
| `git merge feature1 -m "message"`| Merge `feature1` into `main`.                   |  

---

## **Merge Conflicts** ⚔️  
### **Conflict Markers**  
```plaintext
<<<<<<< HEAD
code1
=======
code2
>>>>>>> branch
```  
- **Resolving Conflicts:**  
  1. Delete conflict markers and keep the desired code.  
  2. Repeat for all conflicts.  
  3. Commit the changes.  

---

## **Feature Branch Workflow** 🛠️  
### **Steps**  
1. Create a feature branch:  
   ```bash
   git branch new-feature
   git checkout new-feature
   ```  
2. Make changes and commit:  
   ```bash
   git add .
   git commit -m "new feature message"
   ```  
3. Upload to GitHub:  
   ```bash
   git push origin new-feature
   ```  
4. Create a pull request on GitHub.  
5. Merge the feature branch into `main`.  
6. Update local repository:  
   ```bash
   git checkout main
   git pull origin main
   ```  

---

## **Merge Conflicts in Feature Branch Workflow** ⚔️  
### **Steps**  
1. Get latest updates from `main`:  
   ```bash
   git checkout main
   git pull origin main
   ```  
2. Get latest updates from the feature branch:  
   ```bash
   git checkout feature4
   git pull origin feature4
   ```  
3. Merge `main` into the feature branch:  
   ```bash
   git checkout feature4
   git merge main
   ```  
4. Push the resolved branch to GitHub:  
   ```bash
   git push origin feature4
   ```  

---

✅ **Key Takeaway:** Git is a powerful tool for version control. Mastering it will make you a pro at managing code! 🚀  

--- 

**Happy Coding!** 😊
