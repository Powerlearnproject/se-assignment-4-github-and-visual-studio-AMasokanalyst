[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/GvXCZgfk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15334315&assignment_repo_type=AssignmentRepo)
# SE-Assignment-4
Assignment: GitHub and Visual Studio
Instructions:
Answer the following questions based on your understanding of GitHub and Visual Studio. Provide detailed explanations and examples where appropriate.

Questions:
Introduction to GitHub:

What is GitHub, and what are its primary functions and features? Explain how it supports collaborative software development.

GitHub is a web-based platform for version control and collaborative software development, utilizing Git, a distributed version control system, to manage and track code changes. github has features, such as repositories, version control, collaboration tools, code hosting management, documentation, security features, and community and social coding. 

Primary features and functions of Github

Repositories:
Is a central storage space for projects, containing all project files and revision history. Github has an option to either make repositories public or private. Public repositories are visible to everyone, while private repositories are only visible to the owner and the collaborators.

Version Control:
Tracks changes in code over time, allowing developers to revert to previous versions. It has fundamental aspects such as branching and merging.

Collaboration Tools:
Offers different options such as pull request, issues and projects. Pull Requests allows developers to notify team members about changes pushed to a branch. Issues provides an issue tracker for managing tasks, enhancements, and bugs. Projects helps manage and organize work with Kanban-style boards.

Code Hosting and Management:
Hosts code repositories in the cloud and supports Git Large File Storage. Allows for continuous integration/continuous deployment (CI/CD) through GitHub Actions.

Documentation:
Include GitHub pages that hosts websites directly from a repository, thereby providing an option to have each repository to have an associated wiki.

Security Features:
Security features offered by Github include dependency graphs, security advisories and code scanning. Dependency Graphs visualizes dependencies and vulnerabilities. Security Advisories creates and views advisories for repositories. Code Scanning are automated code reviews used to detect vulnerabilities and coding errors.

Community and Social Coding:
Github offers an easy way for software developer to be able to interact with each other's work by forking. Forking is used to copy a repository to your GitHub account, make changes, and propose merging back to the original project.

GitHub facilitates collaborative software development through distributed workflows, code reviews, task management, automated workflows, and community contributions. It allows multiple developers to work on different parts of a project, enables code reviews, and facilitates automated testing and deployment processes. It also allows developers to fork repositories and contribute back to the original project.

Repositories on GitHub:

What is a GitHub repository? Describe how to create a new repository and the essential elements that should be included in it.

A GitHub repository is a platform that allows users to manage, organize, and track their code, fostering collaboration and continuous improvement.

GitHub Repository Creation

• Log in and click profile icon, then select "New repository."

• Choose name and optional description.

• Set repository visibility either public or private.

• Initialize with README.

• Click "Create repository."

Essential Elements

READ ME: Explain the goal of your project and its intended use.

gitignore: Indicate certain files or directories—such as sensitive data or build artifacts—to ignore.

License: To make it clear to others how they can use your code, use an open-source license (such as MIT or Apache).

Version Control with Git:

Explain the concept of version control in the context of Git. How does GitHub enhance version control for developers?

Git is an open-source version control system that enables developers to continuously update their projects, keeping revisions in a central repository for easy access. GitHub is a cloud-based platform developed around the Git tool, which is used to store source code for projects and maintain the complete history of all changes made to those files. The primary distinction is that, whereas GitHub is an online site that developers using Git may connect to and post or download files, Git is software that developers can install locally on a system to manage source code. Git repositories can be hosted on GitHub.


Branching and Merging in GitHub:

What are branches in GitHub, and why are they important? Describe the process of creating a branch, making changes, and merging it back into the main branch.

GitHub branches are used to establish distinct development streams. Because of this, developers can work on several features or bug fixes at the same time without having an impact on the main codebase. Moreover, branches facilitate project collaboration with other developers. When a developer is ready, they can work on their own branch and merge their modifications into the main branch.

Creating a new Github branch

• Navigate to a desired repository.

• Locate branch selector dropdown (it usually displays default branch name) on main page.

• Type new branch name in dropdown.

• Press Enter to create branch.

• GitHub will automatically create new branch from checked out branch.

Reviewing and Merging the Pull Request

Review the Pull Request: 
You or your collaborators can review the pull request. This can include looking at the code changes, running tests, and discussing any issues in the pull request comments.

Merge the Pull Request: 
Once the changes are reviewed and approved, click the "Merge pull request" button and then confirm the merge by clicking "Confirm merge".

Delete the Branch (optional): 
After merging, you can delete the branch to keep your repository tidy by clicking the "Delete branch" button.

Creating Branches using command line interface

    1. Clone the repository
        git clone  https://github.com/username/repository.git
        cd repository

    2. Creaating and switching to a new branch
        git checkout -b new-branch-name

    3. Staging and commiting changes
        git add .
        git commit -m "Description of the changes"

    4. Pushing the new branch to github
        git push origin new-branch-name         

Pull Requests and Code Reviews:

What is a pull request in GitHub, and how does it facilitate code reviews and collaboration? Outline the steps to create and review a pull request.

Forking a repository allows us to work with it separately, obtaining an instance of the entire repository's history and allowing us to modify it without affecting the original version, this is where pull request comes in. A pull request in GitHub is a proposal to merge a set of changes from one branch into another. We contribute to collaborative projects or open-source projects through pull requests.

Creating Pull Request

    • Navigate to repository's main page.

    • Choose branch with commits.

    • Click "Compare & pull request" in yellow banner.

    • Provide changes details.

    • Submit pull request.

Reviewing Pull Request:

    • Examine changes.

    • Leave comments, suggest improvements, approve pull request.

    • Discuss concerns or questions.

Once approved, the changes can be merged into the default branch.

GitHub Actions:

Explain what GitHub Actions are and how they can be used to automate workflows. Provide an example of a simple CI/CD pipeline using GitHub Actions.

Github Actions is a powerfull automation tool imbedded on Github. Github Actions functions as a plugin for intricate workflow chores by enabling shell commands against repository code that are triggered by events such as commit, pull request, or scheduling. By creating workflows that respond to events, you can automate tasks such as running tests, linting code, deploying applications, and more. Github Actions automation not only saves time but also reduces the potential for human error, making your software delivery process more efficient and reliable.

Automated Workflow Creation

    • Define Workflow File: Create a.github/workflows directory and a YAML file to define the workflow.

    • Specify Events: Use the on key to trigger the workflow on pull_request events.

    • Define Jobs: Use the jobs key to define specific jobs to run, with specific steps for each job.

    • Add Actions: Use GitHub Actions or custom scripts to perform tasks like code checking, dependency setup, testing, or application deployment.

    Example of continuous integration and continous deployement(CI/CD) workflow

name: CI/CD Pipeline

on:
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'
      - run: npm install
      - run: npm test

  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Install dependencies
        run: npm install
      - name: Run linter
        run: npm run lint

  analyze:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Initialize CodeQL
        uses: github/codeql-action/init@v1
        with:
          languages: javascript
      - name: Perform CodeQL Analysis
        uses: github/codeql-action/analyze@v1

  deploy:
    if: github.event.pull_request.merged == true
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to Production
        run: ./deploy.sh

CI workflows automatically run tests and build processes every time a pull request is created or updated. CD automatically deploy applications to staging or production environments when pull requests are merged.


Introduction to Visual Studio:

What is Visual Studio, and what are its key features? How does it differ from Visual Studio Code?

Microsoft's Visual Studio is an IDE that is designed to be used with multiple programming languages and development tools. It is a complete suite of tools for creating applications that can be used on a variety of platforms, such as Windows, the web, mobile devices, and cloud computing. Visual studio code is also a product of microsoft, however it differs from visual studio in that it is a lightweight, open-source code editor that is highly expandable, enabling developers to add features and capabilities through extensions. It is designed to make coding quick and easy.

Difference between visual studio and visual studio code

Type:	
Visual Studio is a full-fledged IDE	while VS Code is a text editor (AKA Code editor).

Platform:	
Visual Studio runs on Windows and Mac while	VS Code runs on Windows, Mac, and Linux.

Size:	
Visual Studio is relatively large. You might have to download more than 40 GB on Windows and over 6 GB on Mac while	VS Code does not require more than 200 MB on any platform.

Support:
Visual Studio has built in support for C# and .NET, alongside several common languages apart from Java. VS Code supports JavaScript, Typescript, and Node JS out of the box. VS code also supports other programming languages – as long as there’s an extension(s) for that.

Pricing:	
Visual Studio Community Edition is free, but the professional and enterprise editions code $45 and $250 per month respectively.	VS Code is free. Most of the extensions are also free but there are freemium ones

Extensions:	
Visual Studio does not have as many extensions as VS Code. VS Code has numerous professionally and curated extensions for various purposes

Integrating GitHub with Visual Studio:

Describe the steps to integrate a GitHub repository with Visual Studio. How does this integration enhance the development workflow?
Debugging in Visual Studio:

Explain the debugging tools available in Visual Studio. How can developers use these tools to identify and fix issues in their code?
Collaborative Development using GitHub and Visual Studio:

Discuss how GitHub and Visual Studio can be used together to support collaborative development. Provide a real-world example of a project that benefits from this integration.


Submission Guidelines:
Your answers should be well-structured, concise, and to the point.
Provide real-world examples or case studies wherever possible.
Cite any references or sources you use in your answers.
Submit your completed assignment by [due date].
