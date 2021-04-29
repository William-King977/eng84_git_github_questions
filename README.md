# Git and GitHub Interview Questions
* **What are the stages of Git on local host?**
  * ANSWR

* **How can you reset/cancel if you have already run `git add .` command?**
  * `git reset` - reset all the added files from `git add .`
  * `git reset filename` - remove the specified file

* **What is a Git staging area?**
  * It acts as a draft space where one can use `git add` to add files that they want to save for their next commit. One can use `git status` to check the files that are currently in the staging area.

* **Workflow and the stages**
  * ANSWR

* **Git merge and merge conflicts**
  * ANSWR

* **Best practice to resolve git merge conflicts**
  1. On GitBash/Terminal, navigate to the repository with the conflict
  2. Use `git status` to show the conflicted file(s)
  3. Open the conflicted file. The conflicted sections will be surrounded with `<<<<<<< HEAD` and `>>>>>>> branch-a`, and the conflicts are separated by `=======`. An example is shown below:
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
  * ANSWR