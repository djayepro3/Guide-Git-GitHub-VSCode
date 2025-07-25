

# 📘 Git & GitHub with VS Code: A Beginner's Guide

> 📌 **Author:** Dishanand Jayeprokash  
> 🗓️ **Created:** 18 July 2025  
> ✏️ **Last Modified:** 25 July 2025  
> 📘 **Covers:** Installing Git, GitHub and VS Code • Create Repo locally or on GitHub • Git Commands • Tips and Resources

---




---

Welcome to your one-stop guide to mastering **Git** and **GitHub** using **Visual Studio Code**! Whether you're just starting out or need a refresher, this guide will walk you through everything from installation to pushing your first commit 🚀.

---

## 📑 Table of Contents

1. [🛠️ Prerequisites](#️-prerequisites)
2. [⬇️ Installing Git, GitHub & VS Code](#️-installing-git-github--vs-code)
3. [🔧 Setting Up Git in VS Code](#-setting-up-git-in-vs-code)
4. [📁 Creating a Local Repository](#-creating-a-local-repository)
5. [☁️ Pushing to GitHub](#️-pushing-to-github)
6. [📥 Cloning a GitHub Repo](#-cloning-a-github-repo)
7. [💬 Git Commands Explained](#-git-commands-explained)
8. [✍️ Changing Author Info](#️-changing-author-info)
9. [📝 VS Code Editor Tips](#-vs-code-editor-tips)
10. [📚 Resources](#-resources)

---


## 🛠️ Prerequisites

Before we begin, make sure you have:

- A GitHub account → [Sign up here](https://github.com/)
- Basic familiarity with command line (helpful but not required)

## ⬇️ Installing Git, GitHub & VS Code

To get started, you'll need to install the following tools:

- **Git**: [Download Git](https://git-scm.com/downloads) 🧰  
  Git is the version control system that helps you track changes in your code.

- **Visual Studio Code (VS Code)**: [Download VS Code](https://code.visualstudio.com/) 🖥️  
  VS Code is a powerful and lightweight code editor with built-in Git support.

- **GitHub Desktop (optional)**: [Download GitHub Desktop](https://desktop.github.com/) 🖱️  
  A GUI tool to manage your GitHub repositories easily.

Make sure to install Git first so that VS Code can detect it and enable Git features.


---

## 🔧 Setting Up Git in VS Code

Once everything is installed, let’s configure Git for the first time:

1. Open **VS Code**.

2. Open the **Terminal** using:

   * `Ctrl + ~` *(Windows/Linux)* or
   * `Cmd + ~` *(Mac)*
     Or navigate through: **Terminal > New Terminal**

3. Configure your identity so Git knows who you are:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

✅ This sets your name and email globally for all your future commits.

> 💡 *Tip:* Want to use different info for a specific project? Remove `--global`.

You can verify your settings like this:

```bash
git config --global --list
```

---

## 📁 Creating a Local Repository

Let’s create your first local project and version control it with Git!

1. Create a folder for your project and open it in VS Code.
2. Initialize Git:

```bash
git init
```

🔍 **What it does:**

* `git`: invokes the Git tool
* `init`: initializes an empty Git repository in your folder (`.git` hidden folder is created)

3. Add a file, like `README.md`, and type something inside.
4. Save the file (`Ctrl + S`).
5. Stage the file (tell Git to track it):

```bash
git add README.md
```

✅ You can use `git add .` to stage *all* changes.

6. Commit the file:

```bash
git commit -m "Initial commit"
```

💬 **What it means:**

* `commit`: record your staged changes
* `-m`: message flag
* `"Initial commit"`: your message explaining the change

---

## ☁️ Pushing to GitHub

Ready to make your code go live on GitHub? Follow these steps:

1. Create a new repository on [GitHub](https://github.com/new) (don't initialize with a README).
2. In your terminal, link your local project to the GitHub repo:

```bash
git remote add origin https://github.com/yourusername/your-repo.git
```

🧠 **Explanation:**

* `remote add`: add a remote server
* `origin`: alias (default name for GitHub)
* URL: the actual repo link

3. Push your local commits to GitHub:

```bash
git push -u origin main
```

🧠 **Breakdown:**

* `push`: upload your code
* `-u`: set upstream (so future pushes can just use `git push`)
* `origin`: remote name
* `main`: branch you're pushing

---

## 📥 Cloning a GitHub Repo

Let’s say you want to work on an existing repo:

1. Copy the repo’s URL from GitHub.
2. Open **VS Code**, press:

   * `Ctrl + Shift + P` *(Windows/Linux)*
   * `Cmd + Shift + P` *(Mac)*
3. Search for **Git: Clone**
4. Paste the URL and choose where to save it locally.

🎉 VS Code will ask if you want to open the cloned repo — say yes!

---

## 💬 Git Commands Explained

Here’s a quick cheat sheet for some of the most common Git commands:

| Command               | Meaning                                |
| --------------------- | -------------------------------------- |
| `git init`            | Initialize a new Git repo              |
| `git status`          | Show current tracked/untracked changes |
| `git add .`           | Stage all changes                      |
| `git commit -m "msg"` | Commit staged changes with a message   |
| `git log`             | Show commit history                    |
| `git remote -v`       | List connected remotes                 |
| `git push`            | Upload changes to remote               |
| `git pull`            | Download and merge from remote         |

> 💡 Use `git status` often — it's your Git dashboard!

---

## ✍️ Changing Author Info

Need to change the author info *just for one commit*? Use this:

```bash
git commit --amend --author="New Name <new.email@example.com>"
```

👀 This will open your default text editor (usually VS Code).

### What You’ll See:

```
# Please enter the commit message...
Initial commit
```

### What to Do:

* Edit the commit message if needed.
* To save and close:

  * Press `Ctrl + S` to save
  * Close the tab, or press `Ctrl + Q` (or `Cmd + W` on Mac)

🎯 This will update both the commit message (if changed) and the author info.

---

## 📝 VS Code Editor Tips

Make the most out of Git inside VS Code! Here are some pro tips:

* 🧭 **Source Control Panel**: Click the Git icon on the sidebar to visually see changes, stage, commit, and push.
* 🔍 **View Diffs**: Click on modified files to see side-by-side diffs.
* 🧠 **GitLens Extension**: Get rich inline Git history and author info.
* ✨ **Markdown Preview**: Preview your README with `Ctrl + Shift + V`.

> 💡 Hover over commit messages in the Source Control panel to see details like author, time, and hash.

---

## 📚 Resources

Here are some helpful links to level up your Git game:

* 📘 [Git Official Documentation](https://git-scm.com/doc)
* 🐙 [GitHub Docs](https://docs.github.com/en)
* 🧪 [Git Handbook by GitHub](https://guides.github.com/introduction/git-handbook/)
* 🧰 [VS Code Git Guide](https://code.visualstudio.com/docs/editor/versioncontrol)

---

## 🙌 Final Words

You did it! 🎉
By following this guide, you’ve:

✅ Installed and configured Git
✅ Used Git inside VS Code
✅ Created and pushed a repository to GitHub
✅ Learned the most important Git commands with confidence!

Now go build something amazing! 💻✨
And don't forget to `git commit` your progress along the way 😉

---





