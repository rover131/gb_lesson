Update
# lesson3

homework

# gb_lesson

## Hello qwer

**hello world!**

1. Fork the instructor's repository: Go to the instructor's repository on GitHub and click the "Fork" button in the top right corner. This will create a copy of the repository under your GitHub account.
2. Clone your forked repository: On your forked repository's page, click the "Code" button and copy the repository's URL. Open a terminal and run the following command to clone the repository to your local machine:

**git clone <repository_url>**

3. Configure upstream remote: Change into the cloned repository's directory using cd <gb_lesson>. Add a remote called "upstream" that points to the instructor's repository:

**git remote add upstream https://github.com/rover131/gb_lesson.git**

4. Fetch upstream changes: Fetch the latest changes from the instructor's repository:

**git fetch upstream**

5. Create a new branch: Create a new branch to work on your changes:

**git checkout -b lesson3**

6. Commit your changes: Stage the modified file and commit your changes with a descriptive commit message:

**git add <file_name>
git commit -m "Add instructions for working with remote repositories"**

7. Push your branch: Push your branch to your forked repository:

**git push origin <branch_name>**

8. Create a pull request: Go to your forked repository on GitHub and switch to the branch you pushed. Click the "Compare & pull request" button next to the branch name. Provide a descriptive title and additional information about your changes, then click "Create pull request."

9. Merge the pull request: Once your pull request is approved, your instructor will merge it into the main repository. Congratulations on successfully contributing to the project!

**git fetch upstream
git checkout main
git merge upstream/main**
