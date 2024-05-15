# Note:-
jab bhi aap ek folder bnaate hai git ko kuchh nahi pata aapke folder ke
baare mein, isliye aap waha pe git ko initialize karte ho, ab git ko
permissions mili hai to git aapke folder ko pehchaanta hai, to ab kyuki
git kaam kar skta hai is folder per ab ham yaha par untracked, tracked
modified, staged, and saved checkpoints create kar skte hai, git kuchh
interesting cheeje kar skta hai jaise ki aap chaahe to kisi bhi moment par
ye check kr skte ho aapki kitni files kis stage par hai


-> initialize karo
-> check kr skte ho aap konsi file kis stage mein hai -> git status -s
-> check kr skte ho aap kitne saved checkpoints hai -> git log --oneline --graph

git status bataata hai file ke changes ke baare mein and uske
baare mein, before commit or after commit

- git status batata hai commit ke phele and baad ki file stages
- git log batata hai, aapke saved points kya hai, aapke saare commit histories




---




## How to Initialize a Git Repository from Visual Studio Code

Follow these steps to initialize a Git repository from Visual Studio Code (VS Code):

### 1. Open Your Project in VS Code

1. Launch Visual Studio Code.
2. Open your project folder by selecting `File > Open Folder` and navigating to your project's directory.

### 2. Open the Source Control View

1. In the sidebar, click on the Source Control icon (or press `Ctrl+Shift+G` on Windows/Linux or `Cmd+Shift+G` on macOS).

### 3. Initialize the Repository

1. In the Source Control view, you should see an option to "Initialize Repository" if your project isn't already a Git repository.
2. Click on the "Initialize Repository" button.

### 4. Confirm Initialization

1. After initializing, you'll see that the Source Control view now shows your project's files with a `U` icon next to them, indicating they are untracked.
2. A new `.git` directory will be created in your project's root directory, containing the Git metadata.

### 5. Make Your First Commit

1. Stage your changes by clicking the `+` icon next to the files you want to include in your commit.
2. Enter a commit message in the input box at the top of the Source Control view.
3. Click the checkmark icon (✔️) or press `Ctrl+Enter` (Windows/Linux) or `Cmd+Enter` (macOS) to make your first commit.




---



## How to Deinitialize a Git Repository

To deinitialize a Git repository, you need to remove the Git tracking information from the directory. Follow these steps:

### 1. Delete the `.git` Directory

The `.git` directory contains all the configuration, history, and metadata for the repository. Deleting this directory will deinitialize the Git repository.

#### For Unix/Linux/macOS:

Open your terminal and navigate to the root directory of your Git repository. Run the following command:

```bash
rm -rf .git
```

#### For Windows (PowerShell):

If the above command doesn't work, use PowerShell to delete the `.git` directory with the following command:

```powershell
Remove-Item -Recurse -Force .git
```

**Note:** Ensure you are in the root directory of the Git repository when you run these commands. This action is irreversible and will remove all Git tracking information.

### 2. Verify Deinitialization

To verify that the repository has been deinitialized, you can run a Git command such as `git status`. You should see an error message indicating that the current directory is not a Git repository:

```bash
git status
```

If you see an error like `fatal: not a git repository (or any of the parent directories): .git`, then the deinitialization was successful.

Alternatively, you can list the contents of the directory to ensure the `.git` directory has been removed:

#### For Windows (PowerShell):

```powershell
Get-ChildItem
```

### Important Note

Deinitializing a Git repository by deleting the `.git` directory will remove all version history and tracking information. If you need to retain this information for future reference, consider creating a backup of the `.git` directory before deleting it.



---


## How to Use a `.gitignore` File in Your Git Repository

A `.gitignore` file specifies which files and directories Git should ignore in a project. This is useful for excluding temporary files, build artifacts, and other files that should not be committed to the repository.

### Steps to Create and Use a `.gitignore` File

### 1. Create a `.gitignore` File

1. Open your project in Visual Studio Code.
2. In the Explorer sidebar, right-click in the file list area and select `New File`.
3. Name the file `.gitignore`.

### 2. Add Patterns to the `.gitignore` File

1. Open the `.gitignore` file you just created.
2. Add file and directory patterns to the file. Each pattern specifies files and directories to ignore.

#### Common Patterns

- Ignore all `.log` files:

  ```plaintext
  *.log
  ```

- Ignore the `node_modules` directory (common for Node.js projects):

  ```plaintext
  node_modules/
  ```

- Ignore build artifacts (example for a Python project):

  ```plaintext
  __pycache__/
  *.pyc
  ```

- Ignore environment variable files:

  ```plaintext
  .env
  ```

### 3. Save the `.gitignore` File

1. After adding the necessary patterns, save the `.gitignore` file (`Ctrl+S` on Windows/Linux or `Cmd+S` on macOS).

### 4. Verify the `.gitignore` File

1. Open the Source Control view in VS Code (`Ctrl+Shift+G` on Windows/Linux or `Cmd+Shift+G` on macOS).
2. Check that the files and directories specified in the `.gitignore` file are not listed under "Changes".

### Example `.gitignore` File

Here is an example of a `.gitignore` file for a Node.js project:

```plaintext
# Logs
*.log

# Dependency directory
node_modules/

# Build output
dist/

# Environment variables
.env

# Temporary files
tmp/
```

### Summary

- **Create File**: Create a `.gitignore` file in your project root.
- **Add Patterns**: Specify file and directory patterns to ignore.
- **Save File**: Save the `.gitignore` file.
- **Verify**: Check that specified files are ignored in the Source Control view.

Using a `.gitignore` file helps keep your repository clean by excluding files that should not be tracked by Git.

---


# Deleting the branch
- git branch 
- git branch -d "branch name (for ex- feature/navbar)"


# how to create and switch to a branch
- git switch -C feature/add-footer