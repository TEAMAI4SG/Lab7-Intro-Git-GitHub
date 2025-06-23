# Lab 7: Introduction to Git and GitHub

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

   a. This command should return the installed version of Git. 

```Python
git --version
```

8. Set up Git: Configure your Git username and email. Begin by typing the following code in the terminal. **Use your actual name and email address.**

   a. These commands will set your global Git configuration to identify your              commits.

```Python
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

9. Initialize a Repository:

    a. The following code sets up a new Git repository in the current directory,           creating a ‘.git’ folder that tracks all changes. 

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

  1) echo "# PROJECTS" > README.md: Prints the string # PROJECTS.
  2) **"> README.md:"** Redirects the printed string into a new file named               README.md.

3) The content **# PROJECTS** added to **README.md** uses Markdown syntax. The **#** symbol indicates that "PROJECTS" is a top-level heading. This simple content serves as a placeholder and can be expanded later with more detailed information about the project. **You can check the content of the “README.md” file in your folder.**

```Python
echo "# PROJECTS" > README.md
```


4) Stage the file for commit:

- The command below adds ‘README.md’ to the staging area, meaning it is ready to be committed to your project.

```Python
git add README.md
```

5) Commit the file:

- The following command creates a commit with the message “Initial commit,” which captures the current state of the staged files. 
- When creating a commit, the message can be anything you want, but it is helpful to be descriptive. A descriptive commit message allows you to know what changes were made with each commit. This practice makes it easier to track your progress and backtrack to identify where any errors may have occurred.

```Python
git commit -m "Initial commit"
```

---

## 🗂️ Working with Branches

1. We will create and manage branches in Git using VS Code.

   a. Create and switch to a new branch called ‘feature’:
     1) The command below creates a new branch named ‘feature’ and switches to it.
     2) Switching to a new branch means that any changes you make to your project          will stay within this branch until you merge it back into the main branch.          This allows you to work on new features or experiments in isolation                 without affecting the main codebase.


```Python
git checkout -b feature
```


b. Make changes in the New Branch:
   
   - Modify the ‘README.md’ file and commit the changes:
      1) The following appends the text “This is a new feature.” to the ‘README.md’         file, stages the changes, and commits them with the message “Add new                features”.


```Python
echo "This is a new feature." >> README.md
git add README.md
git commit -m "Add new feature"
``` 


   c. Check which branch you are in by typing the below command in your Git Bash          terminal.

```Python
git branch
```


   d. Merge the Feature Branch into Main:

   - The code below will allow you to switch back to the ‘main’ branch and merge         the ‘feature’ branch:
     1) The first line of the code switches to the ‘main’ branch
     2) The second line of the code merges the changes from the ‘feature’ branch            into it. 

```Python
git checkout main
git merge feature
```

---


## ☁️ Part 2: Introduction to GitHub

Github is a web-based platform that provides hosting for software development and version control using Git. It offers distributed version control and source code management functionality. GitHub also provides additional features such as bug tracking, feature requests, task management and wikis for every project. This helps developers collaborate, keep track of changes, and manage their projects more efficiently. 

## 🧩 Key features of GitHub include:

1. **Repositories**: A repository (or “repo”) is a storage space where your project files and their revision history are kept. It serves as the central hub for your project, containing all the code, documentation, and other essential files. Repositories can be either public or private, allowing you to control who has access to your project. Public repositories are accessible to anyone, making them ideal for open-source projects. In contrast, private repositories restrict access to only those you explicitly share them with, which is useful for sensitive projects or controlled collaboration.

2. **Commits**: Commits are snapshots of your project at a specific point in time. Each commit records changes made to the repository, capturing the state of the project files and providing a detailed history of modifications. This enables you to track the evolution of your project, understand what changes were made, and by whom. Descriptive commit messages are important as they provide context for the changes, making it easier to navigate the project's history and revert to previous states if necessary.

3. **Branches**: Branches allow you to develop features, fix bugs, or safely experiment with new ideas in a contained area of your repository. By creating a branch, you can work on changes without affecting the main codebase. Once the changes are ready and tested, you can merge the branch back into the main branch. This workflow enables parallel development and helps maintain a stable main codebase while facilitating collaboration among team members. 

4. **Pull Requests**: Pull requests let you propose changes to a repository. They are an essential part of the collaboration workflow on GitHub, allowing contributors to review, discuss, and approve changes before they are merged into the main branch. A pull request includes the changes made in a branch, a description of the modifications, and a discussion thread where reviewers can provide feedback. This process ensures that changes are vetted and agreed upon by the team, maintaining the quality and integrity of the codebase. 

5. **Issues**: Issues are used to track tasks, enhancements, and bugs for your projects. They serve as a centralized place to report problems, suggest new features, and organize work. Each issue can be assigned to contributors, labeled for categorization, and linked to milestones for tracking progress toward specific goals. Issues facilitate project management by keeping track of work items and enabling collaboration among team members to resolve them. 

6. **Project Boards**: Project boards help you organize and prioritize your work. They provide a visual interface to manage projects, track progress, and collaborate with your team. You can create boards with columns representing different stages of work, such as "To Do," "In Progress," and "Done." Cards, which can be issues or pull requests, are moved between columns as work progresses. Project boards enhance workflow management by offering a clear overview of tasks and their status, helping teams stay organized and focused. 

---

## Lab Starts Here

## 🚀 Creating a GitHub Account

1. **If you don’t have a GitHub account yet**, go to [GitHub](https://github.com/) and click on the ‘sign up’ button in the upper right corner.
2. Fill in the required information, including your username, email address, and password.
3. Follow the prompts to complete the sign-up process. 
4. Make sure to verify your email address by following the link sent to your email. 
 
## 🔍 Exploring GitHub Features

**1. Create a New Repository:**

a. To get to the dashboard:
  1) Look for a link or icon labeled “Dashboard” or similar in the main navigation       menu.
  2) Click on it to access the dashboard, where you can manage your repositories.

b. Click on the new button to create a new repository.

c. Fill in the repository name, description (optional), and choose between a public or private repository. 
A public repository is accessible to anyone, which is great for open-source projects where you want to share your code with the world and allow others to contribute. A private repository, on the other hand, restricts access to only those you explicitly share it with, which is ideal for sensitive projects or when you want to control who can see and contribute to your code.

d. Check the box to initialize the repository with a ‘README’ file.

e. Click ‘Create repository’.

**2. Navigate the Repository:**

a. In your newly created repository, you will see several tabs: **Code, Issues, Pull requests, Actions, Projects, Security, Insights, and Settings.**

b. Explore each tab to understand its purpose:

1) **Code:** This section contains the source code and project files. It is the main section where you can view and manage all the project files.
2) **Issues:** Track bugs, tasks, and feature requests. It is a great way to keep track of tasks and improvements.
3) **Pull requests:** Manage proposed changes from contributors. It allows you to review and discuss changes before they are merged into the main branch.
4) **Actions:** Automate workflows and Continuous Integration/Continuous Deployment (CI/CD) processes. GitHub Actions lets you automate tasks within your repository.
5) **Projects:** Organize and prioritize work project boards. It helps you manage work with Kanban-style boards.
6) **Security:** Manage security and vulnerability and set security policies. It offers various security features to help protect your code.
7) **Insights:** The `Insights` tab provides detailed analytics and visualizations, such as graphs of commit activity over time and code frequency, including additions and detections. 

---

## 📋 Best Practices of Using GitHub

**1. Write meaningful commit messages:**

a. Commit messages should be concise but descriptive, explaining the purpose of the commit.
b. Write commit messages using verb phrases in the imperative mood (e.g., “Add feature,” “Fix bug”).

**2. Use branches effectively:**

a. Create separate branches for new features, bug fixes, and experiments.
b. Keep the **main** branch stable and deployable.

**3. Review and text code:**

a. Use pull requests to review and discuss changes before merging them into the **main** branch. This is how you will collaborate with groupmates when you start on your project.
b. Test your code thoroughly to ensure it works as expected. 

**4. Document your project:**

a. Use the **README** file to provide an overview of your project, how to set it up, and how to contribute. This file does not contain code; it is essentially a text file.

**5. Collaborate and communicate:**

a. Use issues to track tasks and communicate with collaborators.
b. Be clear and respectful in your communication, providing constructive feedback and support. 

---

## 🔐 Part 3: Save API Key as an Environment Variable

**1. Save API Key as an Environment Variable.** Please follow the tutorial below to protect your API key. Follow Section 4. Use Environment Variables in place of your API key in the tutorial [Best Practices for API Key Safety](https://help.openai.com/en/articles/5112595-best-practices-for-api-key-safety.) After this step, nobody can see your API key from your code. This will make collaborating with your team members and the teaching staff much easier and safer.

---

## 📥 Part 4: Clone a GitHub Repository

**Material you might find helpful:**

1. [Sample screenshots after running the code](https://sjsu.instructure.com/courses/1594331/pages/resource-page-code-video-demo-and-screenshots)  
2. [Demo video how to run the code](https://sjsu.instructuremedia.com/embed/5d9ec3d0-7975-40ea-89d3-1f651855096b)

**1. Clone the Repository**: Create a new project called "Tutorial" on VS Code. Then clone the [118i-tutorial](https://github.com/unicode101/118i-tutorial) GitHub Repo on your computer by running the following in VS Code terminal:

```Python
git clone https://github.com/unicode101/118i-tutorial.git
```

**2. Run the cloned project**

**Install Dependencies** Navigate to the cloned project directory and install the required dependencies for each code by using a variation of the following command in the terminal. Please update "name_of_library" with what you are required for each page. This is needed for the Python files that have an import statement at the top of the file. 

```Python
pip3 install name_of_library
```

**3. Run the Project using Streamlit**: Check the terminal to see whether you are under the “118i-tutorial” folder within your project folder. Then run the Streamlit application using the following command you are already familiar with.

```Python
streamlit run main_page.py
```

---

## 💳 Part 5: Disable Auto-recharge

1. Log in to your OpenAI account.
2. Go to your account settings.
3. Locate the "Billing" section and disable the "Auto-Recharge" option.

---

## 🎉 Congratulations, you have successfully finished the lab!

## 📝 Assignment:

**1. Customize your GitHub profile:** Add a profile picture, bio, and other relevant details.
**2. Create a new repository:** Initialize it with a README file and explore its features.
**3. Save your API key securely:** Store it as an environment variable to protect it from accidental exposure.
**4. Clone the provided repository:** Use it as a template for your group project.
**5. Disable auto-recharge on your OpenAI account:** This prevents unexpected charges if your API usage exceeds your expectations. Go to your OpenAI account settings and disable the auto-recharge option.


## 📤 Submission:

- Submit a PDF containing screenshots of:
     -  Your GitHub profile and a link to it. (2 pts)
     -  The repository you created. (2 pts)
     -  You have successfully made API key an environment variable (3 pts)
     -  Your successfully running project in VS Code, showing the output without            error on the browser of the main page AND at least 6 of the 8 sub pages.            **The screenshots should include your terminal as well.**
     -  Your OpenAI account settings with auto-recharge disabled. (2 pts)


--- 

## 🔗 References

[Freecodecamp](https://www.freecodecamp.org/news/git-and-github-for-beginners/)


