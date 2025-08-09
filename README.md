# Git and GitHub for Absolute Beginners

Hello and welcome! This guide is designed for anyone who is just starting their journey in coding and wants to learn how to use **Git** and **GitHub**. Don't worry if you've never heard of them—we'll start from the very beginning.

Git is an essential tool for every developer. It's a **version control system** that helps you track changes to your code over time. Think of it as a super-powered "save" button that keeps a history of everything you do.

GitHub is a platform that hosts your Git projects. It's like a social network for developers, where you can share your code, collaborate with others, and contribute to open-source projects.

This guide will take you step-by-step from installing Git to creating your first project on GitHub. Let's get started!

---

## 1. Getting Started: Installing Git

Before we can start using Git, we need to install it on our computer.

### For Windows

1. Go to the official Git website: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. The download should start automatically.
3. Once the download is complete, run the installer. You can keep the default settings for most of the options.
4. After installation, open the **Command Prompt** or **Git Bash** and type `git --version` to confirm it was installed correctly.

### For macOS

1. The easiest way to install Git is by installing Xcode Command Line Tools. Open your **Terminal** and type: `xcode-select --install`
2. Alternatively, you can download the installer from the official Git website: [https://git-scm.com/download/mac](https://git-scm.com/download/mac)
3. You can also use a package manager like Homebrew: `brew install git`
4. To check if it's installed, open your **Terminal** and type `git --version`.

### For Linux

1. Open your **Terminal**.
2. If you are on a Debian-based system (like Ubuntu), use the command: `sudo apt-get install git`
3. If you are on a Fedora-based system, use: `sudo dnf install git`
4. To verify, type `git --version` in your Terminal.

---

## 2. Setting Up Your Identity

After installing Git, you need to tell it who you are. This information will be attached to every change you make.

1. Open your **Terminal** or **Git Bash**.
2. Set your username (use your GitHub username): `git config --global user.name "Your Name"`
3. Set your email address (use the email you used for GitHub): `git config --global user.email "your.email@example.com"`

You can verify your settings by typing: `git config --list`

---

## 3. The Core Workflow: Add, Commit, Push

Now that Git is installed and you've set up your project, let's learn the three most important commands you'll use every day.

Imagine you've just created or edited a file in your project. Here’s what you need to do:

### Step 1: Stage your changes with `git add`

Before you save your changes, you have to tell Git which files you want to include in your next save. This is called "staging."

Use the following command to stage all your changes:

```sh
git add .

 * The dot (.) tells Git to stage all new and modified files in your current folder.
 * Pro-Tip: If you only want to stage a specific file, you can use git add <filename.txt>.
Step 2: Commit your changes with git commit
After staging, you need to save your changes with a descriptive message. A commit is like taking a snapshot of your project at a specific point in time.
git commit -m "Your descriptive message here"

 * The -m stands for "message".
 * Your message should clearly explain what changes you made. For example: "Add user authentication feature" or "Fix bug in login page."
Step 3: Push your changes to GitHub with git push
The changes you've committed are currently only on your local computer. To upload them to your GitHub repository, you need to "push" them.
git push origin main

 * origin is the default name for your remote GitHub repository.
 * main is the default name of your main branch.
Putting it all together: An example
Let's say you just created a new file named hello.js.
 * Stage the file:
   git add hello.js
 * Commit the change:
   git commit -m "Add hello.js file"
 * Push the commit to GitHub:
   git push origin main
Congratulations! You've just completed the core Git workflow.
---

## 4. Branches and Collaboration

When working on a project, especially with others, you shouldn't make changes directly to the main code. Instead, you create a new "branch" for your work. Think of a branch as a separate timeline or a parallel version of your project.

### Why Use Branches?

* **Safety:** It protects the main working version of your project from breaking.
* **Organization:** It keeps your new features or bug fixes separate until they are ready.
* **Collaboration:** It allows multiple people to work on different things at the same time without interfering with each other.

### How to Create a New Branch

Let's say you want to add a new feature to your project. First, create a new branch:

```sh
git checkout -b new-feature-name

 * git checkout is the command to switch between branches.
 * The -b flag is a shortcut to create a new branch and switch to it at the same time.
After running this command, you are now on the new-feature-name branch. Any commits you make will be saved on this branch.
How to Merge Your Changes
Once you've finished your work on the new branch, you need to merge it back into the main branch.
 * Switch back to the main branch:
   git checkout main
 * Merge your changes:
   git merge new-feature-name
This will combine the changes you made on new-feature-name with the main branch.
Pull Requests (PRs) on GitHub
When you're collaborating with others, you don't merge directly. Instead, you create a Pull Request (PR) on GitHub. A PR is a way to propose your changes and ask others to review them before they are merged.
 * Push your new branch to GitHub:
   git push origin new-feature-name
 * Go to your GitHub repository and you'll see a button to "Compare & pull request."
 * Fill out the form and submit it.
Your teammates can now review your code, leave comments, and eventually merge your changes.
5. Common Problems and How to Fix Them
It's completely normal to encounter errors when you're first using Git. Here are some of the most common issues and how you can resolve them.
Problem 1: You forgot to git add
You made some changes and tried to commit, but Git says: "nothing to commit, working tree clean."
Reason: You forgot to tell Git which files to save.
Solution:
Use git add . to stage your changes first, then run git commit again.
Problem 2: Merge Conflicts
This happens when Git can't automatically combine changes from two different branches. It means two people edited the same part of a file in different ways.
Reason: Git needs you to manually decide which changes to keep.
Solution:
 * Open the file with the conflict. Git will show you the conflicting parts, marked with <<<<<<<, =======, and >>>>>>>.
 * Manually edit the file to keep the changes you want. Remove the <<<<<<<, =======, and >>>>>>> markers.
 * After fixing the file, stage and commit the changes to finalize the merge:
   git add .
git commit -m "Resolve merge conflict"

Problem 3: You want to undo your last commit
You made a mistake in your last commit message or included the wrong files.
Solution:
Use the following command to undo your last commit without losing your changes. The changes will be back in your staging area, and you can commit again with a new message.
git reset HEAD~1

 * HEAD~1 means the commit before the current one.
Problem 4: Your git push fails
Git tells you that your local repository is "behind" the remote one.
Reason: Someone else has pushed new changes to GitHub, and your local copy is not up to date.
Solution:
First, get the latest changes from GitHub using git pull, which is a combination of fetching and merging.
git pull origin main

This will update your local branch with the new changes from GitHub. You may need to resolve any merge conflicts that arise. After a successful git pull, you can then git push your changes.

