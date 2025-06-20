# Lab 6: Introduction to Git and GitHub

---

## 📘 Introduction

In this lab, students will learn the fundamentals of Git and GitHub, two essential tools for version control and collaborative software development. By the end of this lab, students will have a solid foundation of how to initialize a Git repository, track changes, create branches, merge changes, and collaborate using GitHub. 

---

## 🎯 Learning Objectives

- **Understand the Fundamentals of Git**: Gain a foundational understanding of what Git is, including its key concepts such as repositories, commits, branches, and merges.
- **Develop Skills in Using Git for Version Control**: Learn to effectively use Git commands to manage version control, including initializing a repository, tracking changes, and managing branches.
- **Collaborate Using Github**: Learn to use GitHub for collaborative development. 
- **Implement Best Practices for Version Control**: Understand and apply best practices for using Git and GitHub in software development projects, including writing meaningful commit messages and maintaining a clean commit history.


---

## ⏱️ Estimated Time
30 minutes

---

## 💵 Estimated Cost
0-$5 (View your OpenAI usage [here](https://platform.openai.com/usage))

---

## 🧠 Part 1: Introduction to Git

Git is a distributed version control system that allows multiple developers to work on a project simultaneously without overwriting each other’s changes. It helps track changes, revert to previous states, and manage multiple versions of the project efficiently. 

## 📦 Key Concepts:
1. **Repository:**  A repository (or "repo") in Git is a storage space where your project files and their complete history are kept. It serves as the central place for all the code, documentation, and metadata associated with your project.

2. **Commit:** In Git, a commit is a fundamental concept that represents a snapshot of your project at a specific point in time. Each commit captures the state of the project files and records the changes made, allowing for effective tracking and management of the project's history. Accompanied by a descriptive commit message, a commit provides context and clarity about the modifications. Each commit has a unique identifier, metadata such as the author's name and timestamp, and links to parent commits, forming a detailed history of the project's development. Commits are incremental, recording only changes since the last commit, which optimizes storage and efficiency. By organizing changes in the staging area before committing, developers ensure that each commit is logical and cohesive. This process is integral to branching and merging workflows, facilitating collaborative development and parallel work on multiple features or fixes.

3. **Branch:**  A branch in Git is a parallel version of the repository that diverges from the main line of development. It allows you to work on different features, bug fixes, or experiments in isolation from the main codebase. When you create a branch, you're essentially making a copy of the repository at a specific point in time, and any changes you make on this branch won't affect the main line of development (often referred to as the "main" or "master" branch) until you merge the branch back in. This enables multiple developers to work on different tasks simultaneously without interfering with each other's work. Once the work on a branch is complete, it can be merged back into the main branch, incorporating the changes and updating the main codebase.

4. **Merge:** In Git, merging is the process of combining changes from different branches into one branch. This is typically done to integrate the changes made in a feature branch back into the main branch (often called "main" or "master"). When you merge branches, Git takes the changes from the source branch and applies them to the target branch.

---

## Lab Starts Here

## ⚙️ Creating an OpenAI API Key

1. **Download Git**: Ensure Git is installed on your computer. You can download it from [Git’s official website](https://git-scm.com/).
2. **Install Git**. Run the installer and follow the on-screen instructions.
3. We will be using Visual Studio Code as our code editor, and that is where we will interact with Git.
4. Create a new folder on your machine and name it “Projects.”
5. Open VS Code.
6. Go to File → Open Folder → Select Projects folder.


7. Open the Terminal window on VS Code and verify the installation by typing the following command in the terminal:
- This command should return the installed version of Git. 

```Python
git --version
```

8. Set up Git: Configure your Git username and email. Begin by typing the following code in the terminal. **Use your actual name and email address.**
- These commands will set your global Git configuration to identify your commits.

```Python
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

9. Initialize a Repository:
   - The following code sets up a new Git repository in the current directory,           creating a ‘.git’ folder that tracks all changes. 

```Python
git config init
```
**OR**

```Python
git init
```

10. Create a file and make the first commit:

1) Create a new file “README.md” and add some content.
A README file, typically named **README.md**, is a markdown file that provides essential information about a project. It usually includes an overview of the project, instructions on how to set it up and use it, a description of the project's purpose, and any other relevant details that help users and developers understand and contribute to the project. The **.md** extension indicates that the file is written in Markdown, a lightweight markup language that allows for easy formatting of text.

2) The following command creates a **README.md** file with the content in `# PROJECTS`.
- This command does the following:
      - echo "# PROJECTS" > README.md: Prints the string # PROJECTS.
      - > README.md: Redirects the printed string into a new file named README.md.

3) The content **# PROJECTS** added to **README.md** uses Markdown syntax. The **#** symbol indicates that "PROJECTS" is a top-level heading. This simple content serves as a placeholder and can be expanded later with more detailed information about the project. **You can check the content of the “README.md” file in your folder.**


