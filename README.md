# task1
 What's version control?
 Version control is also known as source control, it'sthe practice of tracking and managing changes in files.
  
  What's the difference between Git and Github?
  Git is a popular version control system that allows developers to track changes in their code. GitHub is a code hosting platform used for version control and collaboration. In simple terms, you can use git without Github, but you cannot use GitHub without Git.

  These are 3 other Github alternatives:
  1.GitLab
  2.SourceForge
  3.Gitea

  What's the difference between git fetch and git pull?
  git fetch and git pull are both commands in Git that allows you to update your local repository with changes from a remote repository. however they have different behaviors and purposes.
  1.git fetch:
  git fetch is used to retrieve the latest changes from a remote repository without merging them into your current branch. It updates the remote-tracking branches (e.g., origin/master) that are references to the state of the branches on the remote repository. Here's how it works:

  git fetch contacts the remote repository and fetches all the new commits, branches, and tags.
  It updates your local copy of the remote-tracking branches to reflect the latest state of the remote repository.
  It does not modify your local branches or working directory. It only brings the changes into your local repository.
  After running git fetch, you can examine the changes and decide how to integrate them. For example, you can compare branches, review commits, or run tests before merging the changes into your local branch.

  2.git pull:
  git pull is a combination of two Git commands: git fetch and git merge. It fetches the latest changes from a remote repository and automatically merges them into your current branch. Here's how it works:
  git pull performs a git fetch to retrieve the new commits from the remote repository.
  After the fetch, it automatically merges the fetched changes into your current branch, creating a new merge commit if necessary.
  If there are conflicts between the fetched changes and your local changes, you need to resolve the conflicts manually.

  What's git rebase and the command for it?
  In simple terms, git rebase is a Git command that allows you to move or combine your changes onto a different branch.

  Imagine you're working on a branch called "feature" and another branch called "master" has new commits that you want to include in your work. Instead of merging the changes, git rebase lets you add your commits on top of the latest "master" commits.

  The command for git rebase is:

  git rebase <upstream>
  Here, <upstream> refers to the branch you want to incorporate changes from. For example, if you want to rebase your "feature" branch onto "master", you would run:

  git rebase master
  When you run this command, Git takes your "feature" branch's commits that are not in "master" and replays them on top of "master". This way, your branch gets the latest changes from "master" and appears as if you started your work from the most recent state.

  During the rebase, if Git finds any conflicts between your changes and the latest "master" commits, it will pause and ask you to resolve them. You can manually adjust the code to fix the conflicts.

  After resolving conflicts, you can continue the rebase by running:

  git rebase --continue
  If you change your mind or encounter any issues, you can abort the rebase and go back to the original state by running:

  git rebase --abort
  Remember, be cautious when using git rebase on branches that others are using, as it modifies the commit history. It's generally safe to use on your own branches. 

  what' git cherry-pick and the command for it?
   In simple terms, git cherry-pick is a Git command that lets you copy a specific commit from one branch and apply it to another branch.

  The command for git cherry-pick is:

  git cherry-pick <commit>
  Here, <commit> refers to the commit you want to apply to the current branch. You can specify the commit using its unique identifier, often referred to as the commit hash.

  When you run git cherry-pick, Git takes the changes made in the specified commit and applies them to your current branch, creating a new commit. It's like manually selecting and copying a commit's changes and pasting them onto another branch.

  For example, if you have two branches called "branch-A" and "branch-B," and you want to take a specific commit from "branch-A" and apply it to "branch-B," you would use:

  git cherry-pick <commit-hash>
  Git will copy the changes from the specified commit and create a new commit on "branch-B" with those changes.

  
  git cherry-pick is useful when you want to bring specific changes from one branch into another, without merging the entire branch or modifying the commit history. It allows you to pick and choose individual commits to incorporate into your current branch.
