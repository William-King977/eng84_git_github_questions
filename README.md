# Git and GitHub Interview Questions
* **What are the stages of Git on the local host?**
  * **Working Directory**
    * Use `git init` to ensure the file location is Git tracked
    * The above also creates a Git repository
    * The file location will hold a hidden `.git` file
  * **Staging Area**
    * Use `git add` to add files for a commit
    * Use `git status` to view the current staging area contents
  * **Repository**
    * Use `git commit -m "message"` to save the changes to the local repository
    * The commit records the author and time of the commit

* **How can you reset/cancel if you have already run `git add .` command?**
  * `git reset` - reset all the added files from `git add .`
  * `git reset filename` - remove the specified file

* **What is a Git staging area?**
  * It acts as a draft space where one can use `git add` to add the files that they want to save for their next commit. One can use `git status` to check the files that are currently in the staging area.

* **Workflow and the stages**
  1. **Create a branch** - ensures changes made do not affect the main/master branch
  2. **Add commits** - making changes and updates to the branch
  3. **Open a pull request** - notifies that changes have been made and is a request for a code review
  4. **Code review** - a review about the commits made
  5. **Deploy** - once the pull request has been reviewed and the branch passes the tests, the changes can be deployed to verify them in production.
  6. **Merge** - once the changes have been verified in production, merge the changes with the main/master branch.

* **Git merge and merge conflicts**
  * **Git Merge:** When the contents of a source branch is integrated with a target branch. This effectively updates the target branch, but the source branch remains unchanged. 
  * **Git Merge Conflicts:** When a merge cannot be performed between two branches due to making commits on both branches that alter the same line(s) in conflicting ways.

* **Best practice to resolve Git merge conflicts**
  1. On GitBash/Terminal, navigate to the repository with the conflict
  2. Use `git status` to show the conflicted file(s)
  3. Open the conflicted file. The conflicted sections will be surrounded with `<<<<<<< HEAD` and `>>>>>>> commit/branch-name`, and the conflicts are separated by `=======`. An example is shown below:
  
     ```
     Some of my favourite notes:
	   <<<<<<< HEAD
	   * This is different to GitHub, from the local Git repo.
     * Who won? Well, we'll find out in June! From Git repo.
	   =======
	   * The change on the main branch on GitHub
     * Who's going to win WSM 2021? From GitHub test repo
	   >>>>>>> commit/branch-name
     ```
  4. After the conflicts have been resolved, remove the characters mentioned in the previous step to mark it as resolved.
  5. Now, the changes can be added, committed, and pushed to GitHub.

* **Best practices of Git and GitHub**
  * Don't push to the main/master branch
  * Commit often (small **working** changes)
  * Write meaningful commit messages
  * Don't commit dependencies
  * Don't commit sensitive information
  * Create a `.gitignore` file
