# **🚀 GitHub Workflow with Visual Studio Code on Windows**

This guide walks you through using **GitHub** with **Visual Studio Code (VS Code)** on **Windows**, covering installation, configuration, repository creation, pushing changes, and handling pull requests using **VS Code commands**.

---

## **👥 Prerequisites**

Before you begin, ensure that the following tools are installed:

- **[Git for Windows](https://git-scm.com/download/win)**
- **[Visual Studio Code](https://code.visualstudio.com/Download)**
- A **GitHub account** (if you don’t have one, [sign up here](https://github.com/join))

---

## **1️⃣ Install Git for Windows**

To interact with GitHub repositories, you’ll need to install Git.

1. **Download** Git for Windows from [this link](https://git-scm.com/download/win).
2. **Run the installer** and follow the prompts:
   - Choose **"Use Git from Git Bash only"**.
   - Ensure **OpenSSH** is selected for key management.

---

## **2️⃣ Install Visual Studio Code (VS Code)**

1. **Download** the installer from [VS Code’s website](https://code.visualstudio.com/).
2. **Run the installer** and follow the on-screen instructions.

---

## **3️⃣ Open VS Code and Configure Git**

Once Git and VS Code are installed, open **VS Code** and configure your Git username and email.

1. **Open the integrated terminal** by pressing `Ctrl+\`` in VS Code.
2. **Run the following commands to configure Git**:

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your-email@example.com"
   ```

   This will set your global Git configuration, so your commits are associated with the correct identity.

---

## **4️⃣ Clone an Existing GitHub Repository**

To clone an existing GitHub repository directly from VS Code, follow these steps:

1. **Open VS Code** and press `Ctrl+Shift+P` to open the **Command Palette**.
2. Type `Git: Clone` and select it from the dropdown.
3. **Paste the repository URL** you want to clone (either HTTPS or SSH).
4. **Choose the local folder** where you want to save the repository.

VS Code will automatically clone the repository and open it in your editor.

---

## **5️⃣ Check Remote Repository URLs**

To verify the remote repositories linked to your local Git repository, use the following command:

```bash
git remote -v
```

This will display the fetch and push URLs of the remote repository, helping you confirm that you are pushing changes to the correct repository.

Example output:

```bash
origin  https://github.com/your-username/my-repo.git (fetch)
origin  https://github.com/your-username/my-repo.git (push)
```

---

## **6️⃣ Pull Latest Changes with Rebase**

To update your local branch with the latest changes from the remote repository while maintaining a clean commit history, use:

```bash
git pull --rebase origin main
```

### **Why Use `git pull --rebase` Instead of `git pull`?**
- Prevents unnecessary merge commits.
- Keeps a linear commit history.
- Reduces conflicts when collaborating with others.

If you encounter conflicts while rebasing, Git will pause and allow you to resolve them manually before continuing with:

```bash
git rebase --continue
```

To abort the rebase and return to the previous state, use:

```bash
git rebase --abort
```

---

## **7️⃣ Push Changes to GitHub**

Once you’ve made your changes and committed them, push them to GitHub:

```bash
git push origin main
```

If you are working on a new branch:

```bash
git push -u origin feature-branch
```

---

## **💡 Additional GitHub Tips**

- **Sync your local repository**: Keep your local copy updated by running:
  ```bash
  git pull origin main
  ```
- **Use Issues to Track Bugs/Feature Requests**: GitHub’s issue tracker can be integrated with your workflow in VS Code. You can create new issues directly from the GitHub interface.

---

## **🎯 Conclusion**

With these steps, you now know how to:

- Install and configure **Git** and **VS Code**.
- Clone, push, and create repositories and branches in **GitHub**.
- Use `git remote -v` to verify repository URLs.
- Use `git pull --rebase origin main` to keep your history clean.
- Use **VS Code commands** for managing your Git workflow.

---

## **📚 Additional Resources**

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)

