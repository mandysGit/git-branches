### What is a commit?

- Git can be thought of as a timeline management utility ⏳
- A **commit** is a snapshot 📸 of what the project looked like when it was saved at a certain point in time.
  - Every commit has a **SHA**
  - Every commit has the changes that were made in that commit.  `git show` to see those changes. 
- Play video games? You're playing your videogame and your character dies, you can always go back to when you last saved the game before your charater died. 🎮👾 



### What is a SHA?

- Stands for Secure Hash Algorithm  🔒
- it looks something like, ` e2675e151a18082b19f00461e9b581b6b2dd2937`
- SHA uniquely identifies a commit
- Why is SHA important? **Security and Integrity.** We cannot mess around and change a commit.



### Commits are in a linked list data structure.



### What is a linked list?

- nodes with pointers pointing to another node in a direction
- A commit point to their parent commit

![singly linked list](https://github.com/mandysGit/git-branches/blob/main/singly-linked-list.jpg)

- linked lists are a **conceptual** data structure

- Side note: One way to implement a linked list in Javascript is shown here in this [article](https://www.geeksforgeeks.org/implementation-linkedlist-javascript/)

  

### Benefits of linked lists for memory?

Linked lists are memory efficient. We can compare them to Arrays. Arrays take up a chunk of fixed space, whereas linked lists are more free flowing and will take up space where there's space available.

**Array:**

![array](https://github.com/mandysGit/git-branches/blob/main/array.jpg)

**Linked list:**

![linked list](https://github.com/mandysGit/git-branches/blob/main/linked-list.jpg)



### What is a Branch?

- A branch pointer to a commit SHA

- ```
  main ------> 2e92da
  new-feature -----> 23wsdf3
  experiment ------> 87d8d8d
  ```

- You can type this in the root of your git repo to see what your master branch points to

- `cat .git/refs/heads/master`

  

### Git Branching commands

[Git Cheatsheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

[Info on how to get out of sticky situations/mistakes made with commits](https://ohshitgit.com/)

- `git pull` - ❗️**important:** get the latest version of **main** before you create a branch
- `git branch`  - Lists all your branches
- `git branch [branch-name]` Create a new branch at the current commit
- `git checkout [branch-name]` - Switch to another branch
- `git checkout -b [branch-name]` - Create and checkout a new branch
- `git branch -D [branch-name]` - Delete a branch locally



### How to push your branch to remote

- `git push` 
- You may need to add a remote upstream
- upstream is a name for the main repo where you pull and push to



### DEMO

- How to open a PR
- How to do a code review, approve, and merge to main in Github



### How to update your branch with main

❗️**Important**: Before pushing your branch to remote/origin, pull main, and rebase your branch with main. You should do this if origin main has been updated/diverged from your local version of main while you were working on your feature branch. Ask me if you have any questions about this! Have fun! 🥳

**Steps to rebase:**

- `git checkout main`

- `git pull `

- `git checkout [branch-name]`

- `git rebase main`

- or `git rebase main [branch-name]`

- `git push`

- Now your branch should be updated with the latest version of main

  

