# Zendriix Softwares Git Workflow

This repository demonstrates the suggested Git workflow for managing product releases at Zendriix Softwares. Follow these steps to effectively manage your software development process using Git.

## Git Workflow Steps

1.  **Initialize Git Repository**

    ````bash
    git init```
    ````

2.  **Create Branches**
    ````bash
    git checkout -b dev```
    ````
3.  **Develop Features**
    ````bash
    git checkout -b feature-new-feature dev```
    ````
4.  **Commit Changes**
    `bash
    git add .
git commit -m "Implemented new feature"`
5.  **Merge Feature Branch**
    ````bash
    git checkout dev
    git merge --no-ff feature-new-feature```
    ````
6.  **Create Release Branch**
    `bash
    git checkout -b release-1.0 dev`
7.  **Merge into Master**
    `bash
        git checkout master
git merge --no-ff release-1.0`
8.  **Tag the Release**

        ```bash
        git tag -a v1.0 -m "Release version 1.0"```

9.  **Merge Changes Back**
    `bash 
        git checkout dev
git merge --no-ff release-1.0`
10. **Create Hotfix Branch**
    `bash 
    Create Hotfix Branch`
11. **Merge Hotfix**

            ```bash
            git checkout master

    git merge --no-ff hotfix-1.0.1
    git checkout dev
    git merge --no-ff hotfix-1.0.1```

12. **Delete Hotfix Branch**

        ```bash
        git branch -d hotfix-1.0.1```

Repository Structure
The repository structure may include various files and directories representing different branches, versions, and features of your project.

index.html: Sample HTML file.
app.js: Sample JavaScript file.
styles.css: Sample CSS file.
License
This project is licensed under the MIT License - see the LICENSE file for details.
