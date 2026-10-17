# demo_for_git
        Since you are already familiar with committing and pushing your STM32 code to GitHub using VS Code, let's set up a complete GUI-based Git workflow. You will be able to create a branch, save your changes, commit them, and push them to your GitHub repository without typing Git commands in the terminal.
We'll use the Source Control panel in VS Code.
Step 1: Understand the workflow
1. Open your project in VS Code
Your existing STM32 project folder

2. Create a new branch
Example: feature/dwin-ack-handling

3. Stage and commit changes
Use the Source Control buttons

4. Publish or push the branch
Upload your branch to GitHub


Important distinction:
- Branch: A separate line of development for your work.
- Commit: Saves a snapshot of your changes in Git.
- Push: Uploads your commits to GitHub.
- Publish Branch: Pushes a new local branch to GitHub for the first time.
Step 2: Open your existing project
1. Open VS Code.
2. Select File → Open Folder.
3. Select the local folder of your STM32 project that you already connected to GitHub.
4. On the left sidebar, click the Source Control icon.

Keyboard shortcut: Ctrl + Shift + G
You should see your modified files, if there are any. If you see your files listed under Changes, VS Code has detected the Git changes.


If you see Initialize Repository, stop here. It may mean that you opened the wrong folder or that this folder is not currently a Git repository. Don't initialize it again if your existing Git repository is elsewhere.
Step 3: Sign in to GitHub
1. Look for the Accounts icon in the bottom-left corner or the Accounts menu.
2. Select Sign in with GitHub, if available.
3. Complete the browser authentication and return to VS Code.
VS Code's built-in Git support can authenticate with GitHub; you don't need a separate extension just to commit and push. 

Visual Studio Code

Step 4: Create a new branch
For example, suppose you want to work on your DWIN ACK-handling implementation.

1. Click the branch name
Find the current branch name in the bottom-left corner of VS Code. It might say main or master.

2. Select Create New Branch
Choose Create new branch from the menu. If you don't see it, open the Command Palette using Ctrl + Shift + P and search for Git: Create Branch.

3. Enter a branch name
Example:
feature/dwin-ack-handling
Press Enter.

Now check the bottom-left corner. It should show your new branch name.
Important: Create your branch before making new changes. That keeps your feature work separate from the branch you started from.
Step 5: Make changes and stage your files
1. Edit your code as needed and save the files.
2. Open Source Control.
3. Under Changes, click the + icon beside each file you want to include in the commit.

The + icon stages the selected file. You can also hover over Changes and use its + icon to stage all changes.


Review the staged files before continuing. For an STM32 project, make sure you don't accidentally commit temporary build files, generated binaries, or unrelated changes.
Step 6: Commit without using the terminal

1. Enter a commit message
Example:
Implement DWIN ACK handling

2. Click Commit
If VS Code asks whether to stage all changes and commit them, review the files first. Only confirm if that is what you want.



Your changes are now recorded in your local Git history. They are not yet uploaded to GitHub. 

Visual Studio Code
+1

Step 7: Push your branch to GitHub

If this is a new branch
Click Publish Branch in the status bar or Source Control menu. This uploads your branch to the existing GitHub repository and establishes its upstream connection.

For future commits
After committing additional changes, choose Source Control → More Actions (...) → Push. You can also use the available Push button when shown.

If VS Code asks you to authenticate, complete the GitHub sign-in. Then open your GitHub repository in the browser and check the Branches section. Your new branch and its commits should be visible. 

Visual Studio Code
+1

Step 8: Your normal daily workflow
Task	VS Code action
Create a branch	Click branch name → Create New Branch
Check modified files	Source Control → Changes
Stage files	Click +
Commit changes	Enter message → Commit
Upload a new branch	Publish Branch
Upload later commits	More Actions → Push
Download remote updates	More Actions → Pull
Official reference: VS Code Source Control Quickstart.