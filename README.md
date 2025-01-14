**In this project we create 3 files in our local drive then we use some command for checking merge and 
conflict and delete with new branches also we use revert then connect our project to github .
I define a project and issue in Github then adding footer in index.html and then fetch and update my project and close issue.**

**in Github desktop --choose file--clone repository i choose my project and then in this environment i change index.html and add footer then commit push it to Github
in Github i use pull and merge automatically changes add and deleted new branch**
**for syncronize our project from Githun to my desktop Github we can use clone repository from file menu in github desktop software and we can push or pull mor easily**
**all details and command is in this file you can follow it:**

**Part1: 
1-1: create folder "MsProject":**

C:\Users\Elin>cd MsProject
C:\Users\Elin\MsProject>git init
Initialized empty Git repository in C:/Users/Elin/MsProject/.git/

**1-2: create 3 files in that folder**

C:\Users\Elin\MsProject>git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
        script.js
        style.css

nothing added to commit but untracked files present (use "git add" to track)

**1-4: adding and commit 3 files**

C:\Users\Elin\MsProject>git add index.html script.js style.css

C:\Users\Elin\MsProject>git commit -m "First commit with HTML,CSS,Js Files"
[master (root-commit) 3479da6] First commit with HTML,CSS,Js Files
 3 files changed, 21 insertions(+)
 create mode 100644 index.html
 create mode 100644 script.js
 create mode 100644 style.css
 
**Part2:
2-1: create new branch** 

C:\Users\Elin\MsProject>git branch feature/update-title

C:\Users\Elin\MsProject>git branch
  feature/update-title
* master

**2-2:choose new branch**
C:\Users\Elin\MsProject>git checkout feature/update-title
Switched to branch 'feature/update-title'

C:\Users\Elin\MsProject>git branch
* feature/update-title
  master

C:\Users\Elin\MsProject>git status
On branch feature/update-title
nothing to commit, working tree clean

**2-3: change title in index.html**

C:\Users\Elin\MsProject>git status
On branch feature/update-title
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

**2-4: add and commit changes:**
C:\Users\Elin\MsProject>git add index.html

C:\Users\Elin\MsProject>git commit -m "title in index.html is updated"
[feature/update-title 3337059] title in index.html is updated
 1 file changed, 1 insertion(+), 1 deletion(-)
2-5: Mrge and save changes in main root
C:\Users\Elin\MsProject>git checkout master
Switched to branch 'master'

C:\Users\Elin\MsProject>git merge feature/update-title
Updating 3479da6..3337059
Fast-forward
 index.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\Users\Elin\MsProject>git status
On branch master
nothing to commit, working tree clean

**2-6: Delete feature/update-title branch:**

C:\Users\Elin\MsProject>git branch -d feature/update-title
Deleted branch feature/update-title (was 3337059).

C:\Users\Elin\MsProject>git branch
* master
  
**Checking all changes :**

C:\Users\Elin\MsProject>git log
commit 333705933f81d8f7e960cd4b55e1fcb87047d6cc (HEAD -> master)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:54:38 2025 -0800

    title in index.html is updated

commit 3479da602fa2c330f86b2026e46e17f42f49649c
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:49:23 2025 -0800

    First commit with HTML,CSS,Js Files
    
**Part 3
3-1: Create new brach feature/conflict-example**

C:\Users\Elin\MsProject>git branch feature/conflict-example

C:\Users\Elin\MsProject>git branch
  feature/conflict-example
* master
  
**3-2: change branch to new one**

C:\Users\Elin\MsProject>git checkout feature/conflict-example
Switched to branch 'feature/conflict-example'

C:\Users\Elin\MsProject>git branch
* feature/conflict-example
  master
  
**3-3: changes in index.html in new branch**

C:\Users\Elin\MsProject>git status
On branch feature/conflict-example
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

****Save and commit stage ****

C:\Users\Elin\MsProject>git add index.html

C:\Users\Elin\MsProject>git commit -m"conflict feature"
[feature/conflict-example af6cc4f] conflict feature
 1 file changed, 1 insertion(+), 1 deletion(-)
 
**3-4: changing branch to master or main:**

C:\Users\Elin\MsProject>git checkout master
Switched to branch 'master'

C:\Users\Elin\MsProject>git status
On branch master
nothing to commit, working tree clean

C:\Users\Elin\MsProject>git branch
  feature/conflict-example
* master
  
**Changing index.html on main or master branch**

C:\Users\Elin\MsProject>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
3-5: add and commit stage on master main
C:\Users\Elin\MsProject>git add index.html

C:\Users\Elin\MsProject>git commit -m "changes in h in main file"
[master abcf5de] changes in h in main file
 1 file changed, 1 insertion(+), 1 deletion(-)
 
**3-6: Merge and Conflict appear**

C:\Users\Elin\MsProject>git merge feature/conflict-example
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

**3-8: Changing index.html and add and commit stage**

C:\Users\Elin\MsProject>git add index.html

C:\Users\Elin\MsProject>git commit -m "end changes"
[master 7b4c2e4] end changes








C:\Users\Elin\MsProject>git log
commit 7b4c2e49beb79b1fba33d05e5ec429d5d85a0705 (HEAD -> master)
Merge: abcf5de af6cc4f
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:06:47 2025 -0800

    end changes

commit abcf5dea076f739cf890a6f4c95ccb275ab6ffe5
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:03:36 2025 -0800

    changes in h in main file

commit af6cc4f81289e888debb741f93fdefd7255b8a38 (feature/conflict-example)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:01:25 2025 -0800

    conflict feature

commit 333705933f81d8f7e960cd4b55e1fcb87047d6cc
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:54:38 2025 -0800

    title in index.html is updated

commit 3479da602fa2c330f86b2026e46e17f42f49649c
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:49:23 2025 -0800

    First commit with HTML,CSS,Js Files
    
**Part4:
4-1: changing in script.js**

C:\Users\Elin\MsProject>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   script.js

no changes added to commit (use "git add" and/or "git commit -a")

**4-2: add and commit changes (save wrong alarm)**

C:\Users\Elin\MsProject>git add script.js

C:\Users\Elin\MsProject>git commit -m "Adding Wrong Messages in Script.js"
[master 7d465d1] Adding Wrong Messages in Script.js
 1 file changed, 1 insertion(+)

**4-3: check our log**

C:\Users\Elin\MsProject>git log
commit 7d465d11a59b7794adce5290703a46b01fe28305 (HEAD -> master)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:09:34 2025 -0800

    Adding Wrong Messages in Script.js

commit 7b4c2e49beb79b1fba33d05e5ec429d5d85a0705
Merge: abcf5de af6cc4f
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:06:47 2025 -0800

    end changes

commit abcf5dea076f739cf890a6f4c95ccb275ab6ffe5
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:03:36 2025 -0800

    changes in h in main file

commit af6cc4f81289e888debb741f93fdefd7255b8a38 (feature/conflict-example)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:01:25 2025 -0800

    conflict feature

commit 333705933f81d8f7e960cd4b55e1fcb87047d6cc
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:54:38 2025 -0800

    title in index.html is updated

commit 3479da602fa2c330f86b2026e46e17f42f49649c
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:49:23 2025 -0800

    First commit with HTML,CSS,Js Files

**Show log our file:**
C:\Users\Elin\MsProject>git show 7d465d11a59b7794adce5290703a46b01fe28305
commit 7d465d11a59b7794adce5290703a46b01fe28305
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:09:34 2025 -0800

    Adding Wrong Messages in Script.js

diff --git a/script.js b/script.js
index 3cf9980..a8a0b27 100644
--- a/script.js
+++ b/script.js
@@ -1 +1,2 @@
 console.log('!به پروژه من خوش آمدید');
+alert ('این یک هشدار اشتباه است!');

**4-3: revert changes in our file**
C:\Users\Elin\MsProject>git revert  7d465d11a59b7794adce5290703a46b01fe28305
[master aa9e1fc] Revert "Adding Wrong Messages in Script.js"
 1 file changed, 1 deletion(-)

**Check gitlog:**

C:\Users\Elin\MsProject>git log
commit aa9e1fcd4d908923b47474b0f601c6ee3f9b7d82 (HEAD -> master)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:09:58 2025 -0800

    Revert "Adding Wrong Messages in Script.js"

    This reverts commit 7d465d11a59b7794adce5290703a46b01fe28305.

commit 7d465d11a59b7794adce5290703a46b01fe28305
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:09:34 2025 -0800

    Adding Wrong Messages in Script.js

commit 7b4c2e49beb79b1fba33d05e5ec429d5d85a0705
Merge: abcf5de af6cc4f
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:06:47 2025 -0800

    end changes

commit abcf5dea076f739cf890a6f4c95ccb275ab6ffe5
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:03:36 2025 -0800

    changes in h in main file

commit af6cc4f81289e888debb741f93fdefd7255b8a38 (feature/conflict-example)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:01:25 2025 -0800

    conflict feature

commit 333705933f81d8f7e960cd4b55e1fcb87047d6cc
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:54:38 2025 -0800

    title in index.html is updated

commit 3479da602fa2c330f86b2026e46e17f42f49649c
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 10:49:23 2025 -0800

    First commit with HTML,CSS,Js Files




**4-4: Check after revert**


C:\Users\Elin\MsProject>git show aa9e1fcd4d908923b47474b0f601c6ee3f9b7d82
commit aa9e1fcd4d908923b47474b0f601c6ee3f9b7d82 (HEAD -> master)
Author: Azi1403 <azam.digit@gmail.com>
Date:   Mon Jan 13 11:09:58 2025 -0800

    Revert "Adding Wrong Messages in Script.js"

    This reverts commit 7d465d11a59b7794adce5290703a46b01fe28305.

diff --git a/script.js b/script.js
index a8a0b27..3cf9980 100644
--- a/script.js
+++ b/script.js
@@ -1,2 +1 @@
 console.log('!به پروژه من خوش آمدید');
-alert ('این یک هشدار اشتباه است!');



**part 5:**
**create and link our project with Github "published our project"**

C:\Users\Elin\MsProject>git remote add WebProject https://github.com/Azi1403/WebProject.git

C:\Users\Elin\MsProject>git push -u WebProject master
info: please complete authentication in your browser...
Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 8 threads
Compressing objects: 100% (21/21), done.
Writing objects: 100% (21/21), 2.42 KiB | 112.00 KiB/s, done.
Total 21 (delta 6), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (6/6), done.
To https://github.com/Azi1403/WebProject.git
 * [new branch]      master -> master
branch 'master' set up to track 'WebProject/master'.

**5-5: in Github desktop --choose file--clone repository i choose my project and then in this environment i change index.html and add footer then commit push it to Github
in Github i use pull and merge automatically changes add and deleted new branch**
