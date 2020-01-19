<p align=center><i>*** GITHUG CHEATSHEET ***</i></p>

---
```
Name: init
Level: 1
Difficulty: *

A new directory, `git_hug`, has been created; initialize an empty repository in it.
```

Solution:
```sh
git init
```

---
```
Name: config
Level: 2
Difficulty: *

Set up your git name and email, this is important so that your commits can be identified.
```

Solution:
```sh
git config --global user.name <your name>
git config --global user.email <your email ID>
```

---
```
Name: add
Level: 3
Difficulty: *

There is a file in your folder called `README`, you should add it to your staging area
Note: You start each level with a new repo. Don't look for files from the previous one.
```

  Solution:
  ```sh
git add README
```

---
```
Name: commit
Level: 4
Difficulty: *

The `README` file has been added to your staging area, now commit it.
```

Solution:
```sh
git commit -m 'Hi'
```

---
```
Name: clone
Level: 5
Difficulty: *

Clone the repository at https://github.com/Gazler/cloneme.
```

Solution:
```sh
git clone https://github.com/Gazler/cloneme
```

---
```
Name: clone_to_folder
Level: 6
Difficulty: *

Clone the repository at https://github.com/Gazler/cloneme to `my_cloned_repo`.
```

Solution:
  ```sh
git clone https://github.com/Gazler/cloneme my_cloned_repo/
```

---
```
Name: ignore
Level: 7
Difficulty: **

The text editor 'vim' creates files ending in .swp (swap files) for all files that are currently
open. We don't want them creeping into the repository. Make this repository ignore .swp files.
```

Solution:
```sh
echo '*.swp' > .gitignore       # Or enter ".swp" in .gitignore file (create if it doesn't exist).
```

---
```
Name: include
Level: 8
Difficulty: **

Notice a few files with the '.a' extension.  We want git to ignore all but the 'lib.a' file.
```

Solution:
```sh
echo '*.a\n!lib.a' >>.gitignore # Or enter ".a" and "!lib.a" on separate lines in .gitignore file.
```

---
```
Name: status
Level: 9
Difficulty: *

There are some files in this repository, one of the files is untracked, which file is it?
```

Solution:
```sh

git status     # This shows `database.yml` as untracked file. Enter this as file's name.
```

---
```
Name: number_of_files_committed
Level: 10
Difficulty: *

There are some files in this repository, how many of the files will be committed?
```

Solution:
```sh
git status     # It shows 2 files in staging area. Hence 2 files will be committed. Enter 2 as number of files to be committed
```

---
```
Name: rm
Level: 11
Difficulty: **

A file has been removed from the working tree, however the file was not removed from the repository.  Find out what this file was and remove it.
```

Solution:
```sh
git rm deleteme.rb
```

---
```
Name: rm_cached
Level: 12
Difficulty: **

A file has accidentally been added to your staging area, find out which file and remove it from the staging area.  *NOTE* Do not remove the file from the file system, only from git.
```

Solution:
```sh
git rm --cached deleteme.rb
```

---
```
Name: stash
Level: 13
Difficulty: **

You've made some changes and want to work on them later. You should save them, but don't commit them.
```

Solution:
```sh
git stash 
```

---
```
Name: rename
Level: 14
Difficulty: ***

We have a file called `oldfile.txt`. We want to rename it to `newfile.txt` and stage this change.
```

Solution:
```sh
git mv oldfile.txt newfile.txt
```

---
```
Name: restructure
Level: 15
Difficulty: ***

You added some files to your repository, but now realize that your project needs to be restructured.  Make a new folder named `src` and using Git move all of the .html files into this folder.
```

Solution:
```sh
mkdir src
git mv *.html src
```

---
```
Name: log
Level: 16
Difficulty: **

You will be asked for the hash of most recent commit.  You will need to investigate the logs of the repository for this.
```

Solution:
```sh
git log     # Copy the commit ID for the last (and the first) commit. It is hexadecimal ID after 'commit' and '(HEAD -> master)'
```

---
```
Name: tag
Level: 17
Difficulty: **

We have a git repo and we want to tag the current commit with `new_tag`.
```

Solution:
```sh
git tag new_tag
```

---
```
Name: push_tags
Level: 18
Difficulty: **

There are tags in the repository that aren't pushed into remote repository. Push them now.


From /tmp/d20200118-10101-qynt0z/
 * [new branch]      master     -> origin/master
 ```

Solution:
```sh
git push --tags origin master
```

---
```
Name: commit_amend
Level: 19
Difficulty: **

The `README` file has been committed, but it looks like the file `forgotten_file.rb` was missing from the commit.  Add the file and amend your previous commit to include it.
```

Solution:
```sh
git add forgotten_file.rb       # After next command, you will be taken to an editor window. Save it and exit.
git commit --amend
```

---
```
Name: commit_in_future
vel: 20
fficulty: **

Commit your changes with the future date (e.g. tomorrow).
```

Solution:
```sh
git commit --date 13-12-3030 -m "Future commit"
```

---
```
Name: reset
Level: 21
Difficulty: **

There are two files to be committed.  The goal was to add each file as a separate commit, however both were added by accident.  Unstage the file `to_commit_second.rb` using the reset command (don't commit anything).
```

Solution:
```sh
git reset to_commit_second.rb
```

---
```
Name: reset_soft
Level: 22
Difficulty: **

You committed too soon. Now you want to undo the last commit, while keeping the index.
```

Solution:
```sh
git reset HEAD~1 --soft
```

---
```
Name: checkout_file
Level: 23
Difficulty: ***

A file has been modified, but you don't want to keep the modification.  Checkout the `config.rb` file from the last commit.
```

Solution:
```sh
git checkout config.rb 
```

---
```
Name: remote
Level: 24
Difficulty: **

This project has a remote repository.  Identify it.
```

Solution:
```sh
git remote    # Copy and enter name of repository you see (my_remote_repo).
```

---
```
Name: remote_url
Level: 25
Difficulty: **

The remote repositories have a url associated to them.  Please enter the url of remote_location.
```

Solution:
```sh
git config --get remote.remote_location.url # Copy and enter URL you see (https://github.com/githug/not_a_repo).
```

---
```
Name: pull
Level: 26
Difficulty: **

You need to pull changes from your origin repository.
```

Solution:
```sh
git pull origin master
```


---
```
Name: remote_add
Level: 27
Difficulty: **

Add a remote repository called `origin` with the url https://github.com/githug/githug
```

Solution:
```sh
git remote add origin https://github.com/githug/githug
```

---
```
Name: push
Level: 28
Difficulty: ***

Your local master branch has diverged from the remote origin/master branch. Rebase your commit onto origin/master and push it to remote.


warning: no common commits
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
From /tmp/d20200118-29651-1jbkhki/
 * [new branch]      master     -> origin/master
 ```

Solution:
```sh
git rebase origin/master
git push origin master
```

---
```
Name: diff
Level: 29
Difficulty: **

There have been modifications to the `app.rb` file since your last commit.  Find out which line has changed.
```

Solution:
```sh
git diff      # See that line 26 has been changed. Enter 26 when asked next which line has been changed.
```

---
```
Name: blame
Level: 30
Difficulty: **

Someone has put a password inside the file `config.rb` find out who it was.
```

Solution:
```sh
git blame config.rb     # See that "Spider Man" has put the password in the file. Enter "Spider Man" When prompted.
```

---
```
Name: branch
Level: 31
Difficulty: *

You want to work on a piece of code that has the potential to break things, create the branch test_code.
```

Solution:
```sh
git checkout -b test_code
```

---
```
Name: checkout
Level: 32
Difficulty: **

Create and switch to a new branch called my_branch.  You will need to create a branch like you did in the previous level.
```

Solution:
```sh
git checkout -b my_branch
```

---
```
Name: checkout_tag
Level: 33
Difficulty: **

You need to fix a bug in the version 1.2 of your app. Checkout the tag `v1.2`.
```

Solution:
```sh
git checkout v1.2
```

---
```
Name: checkout_tag_over_branch
Level: 34
Difficulty: **

You need to fix a bug in the version 1.2 of your app. Checkout the tag `v1.2` (Note: There is also a branch named `v1.2`).
```

Solution:
```sh
git checkout refs/tags/v1.2
```

---
```
Name: branch_at
Level: 35
Difficulty: ***

You forgot to branch at the previous commit and made a commit on top of it. Create branch test_branch at the commit before the last.
```

Solution:
```sh
git branch test_branch HEAD~1
```

---
```
Name: delete_branch
Level: 36
Difficulty: **

You have created too many branches for your project. There is an old branch in your repo called 'delete_me', you should delete it.
```

Solution:
```sh
git branch -d delete_me 
```

---
```
Name: push_branch
Level: 37
Difficulty: **

You've made some changes to a local branch and want to share it, but aren't yet ready to merge it with the 'master' branch.  Push only 'test_branch' to the remote repository
```

Solution:
```sh
git checkout test_branch
git push origin test_branch
```

---
```
Name: merge
Level: 38
Difficulty: **

We have a file in the branch 'feature'; Let's merge it to the master branch.
```

Solution:
```sh
git merge feature
```

---
```
Name: fetch
Level: 39
Difficulty: **

Looks like a new branch was pushed into our remote repository. Get the changes without merging them with the local repository 
```

Solution:
```sh
git fetch
```

---
```
Name: rebase
Level: 40
Difficulty: **

We are using a git rebase workflow and the feature branch is ready to go into master. Let's rebase the feature branch onto our master branch.
```

Solution:
```sh

git checkout feature
git rebase master
```

---
```
Name: rebase_onto
Level: 41
Difficulty: **

You have created your branch from `wrong_branch` and already made some commits, and you realise that you needed to create your branch from `master`. Rebase your commits onto `master` branch so that you don't have `wrong_branch` commits.
```

Solution:
```sh
git rebase --onto master wrong_branch
```

---
```
Name: repack
Level: 42
Difficulty: **

Optimise how your repository is packaged ensuring that redundant packs are removed.
```

Solution:
```sh
git repack -d
```

---
```
Name: cherry-pick
Level: 43
Difficulty: ***

Your new feature isn't worth the time and you're going to delete it. But it has one commit that fills in `README` file, and you want this commit to be on the master as well.
```

Solution:
```sh
git checkout new-feature 
git log README.md      # Copy the first commit you see topmost.
git checkout master
git cherry-pick <copied commit ID>  # Paste the copied commit ID in last to last step.
```

---
```
Name: grep
Level: 44
Difficulty: **

Your project's deadline approaches, you should evaluate how many TODOs are left in your code
```

Solution:
```sh
git grep TODO       #This gives all lines with TODOs. Count and enter when asked (probably it will be 4).
```

---
```
Name: rename_commit
Level: 45
Difficulty: ***

Correct the typo in the message of your first (non-root) commit.
```

Solution:
```sh
git rebase -i --root
# Edit the commit with message "First coommit" by changing `pick` to `edit` or "e" before the commit message and commit ID.
git commit --amend -m "First commit"`
git rebase --continue 
```

---
```
Name: squash
Level: 46
Difficulty: ****

You have committed several times but would like all those changes to be one commit.
```

Solution:
```sh
git rebase -i --root 
# Now change the prefix of commits with message "(squash this commit into Adding README)" from "pick" to "f" or "fix".
```

---
```
Name: merge_squash
Level: 47
Difficulty: ***

Merge all commits from the long-feature-branch as a single commit.
```

Solution:
```sh
git merge long-feature-branch --squash 
git commit -m "Squashed 'em all!"
```

---
```
Name: reorder
Level: 48
Difficulty: ****

You have committed several times but in the wrong order. Please reorder your commits.
```

Solution:
```sh
git rebase -i --root
# Reorder commits by cut and paste so that they are in descending order as shown:
# Third commit
# Second commit
# First commit
# Initial Setup
```

---
```
Name: bisect
Level: 49
Difficulty: ***

A bug was introduced somewhere along the way.  You know that running `ruby prog.rb 5` should output 15.  You can also run `make test`.  What are the first 7 chars of the hash of the commit that introduced the bug.
```

 Steps for solution:
 1. Run `git bisect start`.
 2. Run `ruby prog.rb 5` and every time you get result `15`, run `git bisect good`. If result of `ruby prog.rb 5` is not `15`, run `git bisect bad`. Do this repeatedly after next step.
 3. Get the commit ID of first commit (by `git log` and seeing ID of first entry). And execute `git checkout <first commit ID>`. Continue step 2 unless you get "first bad commit" with a  commit message.
 4. Copy the commit ID and paste in next task when asked.

---
```
Name: stage_lines
evel: 50
ifficulty: ****

You've made changes within a single file that belong to two different features, but neither of the changes are yet staged. Stage only the changes belonging to the first feature.
```

Steps for solution:
1. Open the modified file "feature.rb"
2. Cut the line "This change belongs to the second feature"
3. Save the file.
4. Run `git add feature.rb`
5. Paste the line "This change belongs to the second feature" at the bottom.
6. Save. Task is complete, go for next task.

---
```
Name: find_old_branch
Level: 51
Difficulty: ****

You have been working on a branch but got distracted by a major issue and forgot the name of it. Switch back to that branch.
```

Solution:
```sh
git checkout -
```

---
```
Name: revert
Level: 52
Difficulty: ****

You have committed several times but want to undo the middle commit.
All commits have been pushed, so you can't change existing history.
```

Steps for solution:

1. Use `git log` to see and copy ID of "bad commit".
2. `git revert <commit ID>`.

---
```
Name: restore
Level: 53
Difficulty: ****

You decided to delete your latest commit by running `git reset --hard HEAD^`.  (Not a smart thing to do.)  You then change your mind, and want that commit back.  Restore the deleted commit.
```

Steps for solution:

1. Use `git reflog` to see logs.
2. Copy commit ID for commit to restore.
3. Use `git cherry-pick <commit ID>`.

---
```
Name: conflict
Level: 54
Difficulty: ****

You need to merge mybranch into the current branch (master). But there may be some incorrect changes in mybranch which may cause conflicts. Solve any merge-conflicts you come across and finish the merge.
```

Steps for solution:

1. Use `git merge mybranch`.
2. There are merge conflicts. Open modified file (poem.txt in this case). Check modified file by `git status`.
3. Delete the part:

```
<<<<<<< HEAD
Categorized shoes by color
=======

and

>>>>>>> mybranch↲
```

4. Save the file and execute `git add -u` to add file in staging area.
5. Execute `git merge --continue`, enter a merge message, save and exit.

---
```
Name: submodule
Level: 55
Difficulty: **

You want to include the files from the following repo: `https://github.com/jackmaney/githug-include-me` into a the folder `./githug-include-me`. Do this without manually cloning the repo or copying the files from the repo into this repo.
```

Solution:
```sh
git submodule add https://github.com/jackmaney/githug-include-me githug-include-me/
```

---
```
Name: contribute
Level: 56
Difficulty: ***

This is the final level, the goal is to contribute to this repository by making a pull request on GitHub.  Please note that this level is designed to encourage you to add a valid contribution to Githug, not testing your ability to create a pull request.  Contributions that are likely to be accepted are levels, bug fixes and improved documentation.
```

Solution:

Didn't clear this yet! XD
