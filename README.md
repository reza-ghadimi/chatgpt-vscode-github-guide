---

# **🚀 GitHub Workflow with Visual Studio Code on Windows**

This guide walks you through using **GitHub** with **Visual Studio Code (VS Code)** on **Windows**, covering installation, configuration, repository creation, pushing changes, and handling pull requests using **VS Code commands**.

---

## **📥 Prerequisites**

Before you begin, ensure that the following tools are installed:

- **[[Git](https://git-scm.com/download/win)](https://git-scm.com/download/win)** for Windows
- **[[Visual Studio Code](https://code.visualstudio.com/Download)](https://code.visualstudio.com/Download)**
- A **GitHub account** (if you don’t have one, [[sign up here](https://github.com/join)](https://github.com/join))

---

## **1️⃣ Install Git for Windows**

To interact with GitHub repositories, you’ll need to install Git.

1. **Download** Git for Windows from [[this link](https://git-scm.com/download/win)](https://git-scm.com/download/win).
2. **Run the installer** and follow the prompts:
   - Choose **"Use Git from Git Bash only"**.
   - Ensure **OpenSSH** is selected for key management.

---

## **2️⃣ Install Visual Studio Code (VS Code)**

1. **Download** the installer from [[VS Code’s website](https://code.visualstudio.com/)](https://code.visualstudio.com/).
2. **Run the installer** and follow the on-screen instructions.

---

## **3️⃣ Open VS Code and Configure Git**

Once Git and VS Code are installed, open **VS Code** and configure your Git username and email.

1. **Open the integrated terminal** by pressing `Ctrl+`` in VS Code.
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

## **5️⃣ Create a New Repository on [GitHub](https://github.com/)**

To create a new repository on GitHub directly from VS Code:

1. Go to [GitHub](https://github.com/) and click on the **+** icon in the top-right corner.
2. Select **New repository**.
3. Fill in the repository name (e.g., `my-first-repo`), choose the visibility (public or private), and click **Create repository**.
4. **Copy the remote URL** provided (HTTPS or SSH).

Now, let’s connect this repository to VS Code:

1. Open the **VS Code terminal** (`Ctrl+``) and initialize a new Git repository:
   ```bash
   git init
   ```
2. **Add the GitHub remote URL**:
   ```bash
   git remote add origin https://github.com/your-username/my-first-repo.git
   ```
3. **Add and commit your changes**:
   ```bash
   git add .
   git commit -m "Initial commit"
   ```

4. **Push the changes to GitHub**:
   ```bash
   git push -u origin master
   ```

---

## **6️⃣ Make Changes and Stage Them in VS Code**

Now, let’s modify some files and commit the changes.

1. Open any file in the repository and **make changes**.
2. **Stage changes** by opening the **Source Control** tab (`Ctrl+Shift+G`) and clicking the **+** icon next to the file.
3. **Commit changes** with a message in the **Source Control** panel and hit `Ctrl+Enter`.

---

## **7️⃣ Push Changes to GitHub**

Once you’ve made your changes and committed them, you need to push them to GitHub.

1. In the **Source Control** panel, click on the **...** (ellipsis) and select **Push**.
   
   Alternatively, you can open the terminal and use the following Git command:
   
   ```bash
   git push
   ```

---

## **8️⃣ Create and Switch to a New Branch**

If you’re working on a new feature, it’s best practice to create a new branch.

1. **Open the Command Palette** (`Ctrl+Shift+P`).
2. Type `Git: Create Branch` and select it.
3. Name your new branch (e.g., `feature-xyz`) and press `Enter`.
4. VS Code will automatically switch to the new branch.

Alternatively, use the following command in the terminal:
```bash
git checkout -b feature-xyz
```

---

## **9️⃣ Push a New Branch to GitHub**

After creating your branch, you’ll need to push it to GitHub.

1. First, **commit any changes** you’ve made on your new branch.
2. Open the **Source Control** panel, click on the **...** (ellipsis), and select **Push**.
   
   Or, use the terminal:
   ```bash
   git push -u origin feature-xyz
   ```

---

## **🔟 Create a Pull Request (PR)**

Once you’ve pushed your changes to a new branch, you can create a pull request (PR) on GitHub.

1. **Go to GitHub**, and you should see a notification suggesting you create a pull request for the newly pushed branch.
2. **Click** on **Compare & Pull Request**.
3. Add a **description**, review the changes, and click **Create Pull Request**.

---

## **1️⃣1️⃣ Accept a Pull Request**

As a repository maintainer, you might want to review and accept pull requests.

1. Navigate to the **Pull Requests** tab on your GitHub repository.
2. Select the pull request you want to review.
3. Click **Merge pull request** to merge the changes into the `master` or `main` branch.

---

## **🛠 Additional GitHub Tips**

- **Sync your local repository**: Keep your local copy updated by running `git pull origin master` or `git pull origin main` in the terminal.
- **Use Issues to Track Bugs/Feature Requests**: GitHub’s issue tracker can be integrated with your workflow in VS Code. You can create new issues directly from the GitHub interface.

---

## **🎯 Conclusion**

With these steps, you now know how to:

- Install and configure **Git** and **VS Code**.
- Clone, push, and create repositories and branches in **GitHub**.
- Use **VS Code commands** for managing your Git workflow, including handling pull requests.

---

## **📚 Additional Resources**

- [[Git Documentation](https://git-scm.com/doc)](https://git-scm.com/doc)
- [[GitHub Docs](https://docs.github.com/)](https://docs.github.com/)

---
