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
