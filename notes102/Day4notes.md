Day4 HTML : 6/23/2022 Git Tutorial A Comprehensive Guide: Clink Link [link]( https://blog.udemy.com/git-tutorial-a-comprehensive-guide/)

#This articles tell you some comprehensive of how Terminal (for mac) works
•	_Version Control_ – System allows you to revisit various verisons of a file or set of file by recording changes.
•	_Local Version control_ – Old way of local VCS entails one database on your hard disk that stores changes to files.
•	_Centralized Version Control_-CVS streamlined collaboration process allow programmers to work collaborate with teammate.
•	_Distributed Version Control_-(DVCS) address major vulnerability of the CVS: the server as single point of failure. If a cvs goes down, the collaborators cannot work with each other on a file or save changes and new versions. DVCS allow clients to create mirrored repositories, these data backups can be easily placed on the server to replace any lost info. So programmers can collaborate to work varies way to fix the issue on the mirror repositories. 
•	_So what is Git?_
*So, what is Git?
Snapshots
Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.
Local Operations
Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.
Tracking Changes
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.
Loss of Data
Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.
States
Files in Git can reside in three main states: committed, modified and staged.
Committed
Data is securely stored in a local database
Modified
File has been changed but not committed to the database
Top courses in Git

The Git & Github Bootcamp
Colt Steele
4.8  (9,341)
Bestseller

The Ultimate Git Course - with Applications in Unreal Engine
Stephen Ulibarri
4.9  (139)

Rocking Git & GitHub - A Real World Guide
Rajdeep Saha | Cloud Architect @Fortune10 Company
4.9  (65)
Bestseller

Git and GitHub for DevOps Engineers
AR Shankar | Valaxy Technologies
4.7  (225)

Git & GitHub - The Practical Guide
Academind by Maximilian Schwarzmüller, Maximilian Schwarzmüller, Manuel Lorenz
4.7  (2,550)

GitHub Ultimate: Master Git and GitHub - Beginner to Expert
Jason Taylor
4.5  (9,351)

The Complete Git Guide: Understand and master Git and GitHub
Bogdan Stashchuk | Software Engineer, MBA, PhD, CCIE
4.6  (3,164)

Git Mastery: Beginner to Expert with GitHub & GitLab
Mike Kilic
4.5  (165)

Bitbucket Complete: Learn Git with Bitbucket Cloud-Hands On
Mahesha K
4.5  (112)

Git Essentials: Learn Git with Bitbucket and Sourcetree
Juke Moon
4.5  (6,272)

DevOps Project: CICD with Git GitLab Jenkins and Laravel
Dare Soremi
4.7  (222)
Bestseller

Git for Geeks: Quick Git Training for Developers
Jason Taylor
4.6  (1,565)
>
More Git Courses
Staged
Flagged a file’s changed version to be committed in the next snapshot
 
History of Git
Git traces its roots to the open source software project Linux kernel. Developers of this project began using a DVCS called BitKeeper in 2002. In 2005, many of these developers stopped using this DVCS due to tension between the Linux kernel community and the company behind BitKeeper’s and the eventual revocation of the DVCS’ gratis status. Subsequently, Linus Torvalds, the chief architect of the Linux kernel, began creating Git. With the intention of creating a DVCS with a workflow design similar to that of BitKeeper, which was also fast, Git allowed for non-linear development via multiple branches, could support large projects, possessed strong mechanisms preventing corruption, and had a simple design. Since its inception in 2005, Git has become one of the most utilized Version Control Systems in the world.
Getting Started
Download Git
In order to use Git, your computer must have it available. If you already have Git on your computer, you should make sure you have the latest version.
Git can be installed in three ways:
1.	Install as a package
2.	Install via another installer
3.	Download and compile the source code.
Mac OS X
Terminal
The simplest method for installing Git on a Mac (for Mavericks 10.9 and above) is running Git from the Terminal. If Git is not installed, you will see a prompt for installation.
Git Website
You can also download Git by visiting this link and following the posted directions:
http://git-scm.com/download/mac
GitHub
A third option is to install Git as part of the GitHub for Mac install. GitHub is repository hosting service, which we will discuss in a future section.
Download GitHub for Mac via the following link:
http://mac.github.com
Windows
Git Website
You can download Git by visiting this link and following the posted directions:
http://git-scm.com/download/win
GitHub
Install Git as part of the GitHub for Windows install.
http://windows.github.com
Linux
Package Manager
You can try installing Git via your distribution’s inherent package management tool.
For Fedora:
$ sudo yum install git
For Ubuntu:
$ sudo apt-get install git
Git Website
To download Git for Linux, visit this link and follow the posted directions:
http://git-scm.com/download/linux
Graphical Clients
Git includes inherent Graphical User Interface (GUI) tools. However, users can also utilize third-party tools created for particular platforms.
GUI Clients
You can access a variety of GUI clients for Mac, Windows, and Linux via the following link:
https://git-scm.com/downloads/guis
Initial Customization
After making sure Git has been installed, you should perform some customization steps, which should only need to be completed once on any machine. To change settings, you can repeat these steps.
Configuration of Variables
An inherent Git tool called git config allows the setting of configuration variables that control aspects of Git’s operation and look.
Identity Setting
After installing Git, users should immediately set the user name and email address, which will be used for every Git commit.
Type the following into Terminal or Command Line:
git config --global user.name "Jane Smith"

git config --global user.email "example@email.com"
To confirm that you have the correct settings, enter the following command:
git config --global user.name (should return Jane Smith)

git config --global user.email (should return example@email.com)
*By using the –global option, these Git settings apply to anything on the system. To use different identity settings for a specific project, change the working directory to the desired local Git repository and repeat the steps above without using –global.
Default Text Editor
Without configuration of a default text editor, Git will use the system’s default editor–most likely Vim. To configure a different text editor, such as Emacs, type the following into your Terminal or Command Line:
$ git config --global core.editor emacs
Note: For some editors, you may need to find specific instructions for default configuration.
Check Settings
To check settings, use the git config --list command.
Example:
$ git config --list

user.name=Jane Smith

user.email=example@email.com

color.status=auto

color.branch=auto

color.interactive=auto

...
Getting Help
There are three ways to get more information on a particular command, by accessing the manual:
git help command

git command --help

man git-command
Setting up a Git Repository
Importing
To import an existing project or directory into Git, follow these steps using the Terminal or Command Line:
1.	Switch to the target project’s directory
Example:
$ cd test (cd = change directory)
2.	Use the git init command
$ git init
Note: At this stage, you have created a new subdirectory named .git that has the repository files. Tracking has not commenced.
3.	To start tracking these repository files, perform an initial commit by typing the following:
$ git add *.c
$ git add LICENSE
$ git commit -m “any message here”
Now, your files are tracked and there’s an initial commit. We will discuss the particular commands in detail soon.
Cloning
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:
$ git clone https://github.com/test
By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.
To clone a repository into a directory with another name of your choosing, use the following command format:
$ git clone https://github.com/test mydirectory
The command above makes a copy of the target repository in a directory named “mydirectory.”
Workflow
Local Repository Structure
The local Git repository has three components:
1.	Working Directory: The actual files reside here.
2.	Index: The area used for staging
3.	Head: Points to the most recent commit
 
Saving Changes
All files in a checked out (or working) copy of a project file are either in a tracked or untracked state.
Tracked
Tracked files can be modified, unmodified, or staged; they were part of the most recent file snapshot.
Untracked
Untracked files were not in the last snapshot and do not currently reside in the staging area.
*After cloning a repository, files have tracked status and are unmodified because they have been checked out but not edited.
The Life Cycle of File Status
1.	After you edit a file, Git flags it as modified because of changes made after the previous commit.
2.	You stage the modified file.
3.	Then, you commit staged changes.
 
Check File Status
To determine the state of files, utilize the git status command:
$ git status
On branch master
nothing to commit, working directory clean
*This information indicates which branch you’re on (we will cover branches in a later section) and states “working directory clean,” which means that files have tracked or modified status at the moment. Also, no untracked files are present because Git has not listed any.
Tracking and Staging a New File
Single File
Track one file only by using the following format:
git add filename
All Files
Track all files in a repository by using the following command:
$ git add *
*After using these commands, files are tracked and staged for committing.
After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:
$ git status

On branch master

Changes to be committed:

  (use "git reset HEAD ..." to unstage)
new file: EXAMPLE
This information tells us that there are changes to be committed and that the file has been staged.
Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:
$ git commit -m “made change x,y,z”
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.
Committing All Changes
$ git commit -a
*This command commits a snapshot of all modifications to tracked files in the working directory.
Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.
Example:
$ git push origin master
*This command pushes changes from the local “master” branch to the remote repository named “origin”.
*For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local repository. However, these names can be changed by the user.
Git students also learn
GitHub Version Control Distributed Version Control DevOps Jenkins Java SOLID Principles Object Oriented Programming GitLab JavaScript CSS Docker Kubernetes Python
Stashing Changes
When you are not ready to commit changes but do not want to lose them either, git stash is a great option. This command temporarily removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply use the git stash apply command to retrieve the hidden changes.
Remote Repositories
In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.
Cloned Repositories
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.
Seeing Your Remotes
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.
By using git remote -v, you can view all the remote URLs next to their corresponding short names.
$ cd example

$ git remote -v

remote1 https://github.com/remote1/example (fetch)

remote1 https://github.com/remote1/example (push)

remote2 https://github.com/remote2/example (fetch)

remote2 https://github.com/remote2/example (push)

remote3 https://github.com/remote3/example (fetch)

remote3 https://github.com/remote3/example (push)
Adding Remotes
To create a new remote Git repository with a short name, use the following format:
git remote add shortname url
Example:
$ git remote

origin

$ git remote add js https://github.com/janesmith/project1

$ git remote -v

origin https://github.com/johndoe/project1 (fetch)

origin https://github.com/johndoe/project1 (push)

js     https://github.com/janesmith/project1 (fetch)

js     https://github.com/janesmith/project1 (push)
This addition of these remote and short names allows you to use shortnames for Git collaboration.
Fetching
Fetching entails pulling data that you don’t have from a remote project.
Here is the command format:
git fetch [remote-name]
*Now, you should also possess the references to all branches for that remote (more on branching later).
Cloned Repositories
For cloned repositories, use the command git fetch origin to pull down any new changes that were pushed to the server since you cloned or last fetched from it.
 
Note: git fetch solely pulls new data to a local repository; it does not merge changes with or modify your local work. We will discuss merging in a later section. Later, we will also discuss git pull , which allows for fetching and automatic merging.
Pushing
To push your changes “upstream” for sharing, you would use the following git push command format:
git push [remote-name][branch-name]
Example:
$ git push origin master
*This command pushes committed changes from your local “master” branch upstream to the “origin” server.
Note: You can only successfully push changes upstream if you have write access for the server from which you cloned, and if someone else has not pushed changes upstream that you haven’t pulled yet. If a collaborator pushed changes upstream after you had cloned, your push will not be successful. You will have to pull new changes and merge them with your branch before you can successfully push your changes upstream.
Renaming/Removing Remotes
Rename
To rename a remote’s short name, use the git remote rename command.
Example:
$ git remote rename js jane

$ git remote

origin

jane
*In the example above, we can see that the remote’s short name has been changed from js to Jane. The command git remote lists our existing remotes, which jane is now one of. The rename action also alters names of remote branches: js/master would change to jane/master.
Remove
To remove a remote for whatever reason (e.g., a contributor has left the team, the server has moved), simply use the git remote rm command:
Example:
$ git remote rm jane

$ git remote

origin
 
NOTE: Reminder: “origin” is simply the default remote name when you use the git clone command.
Undoing Actions
Git has mechanisms for undoing certain actions.
Commit Mistakes
You can use the –amend command when you need to alter a commit message or forgot to add some files.
$ git commit --amend
In the example above, you can use this command to easily change your commit message, if no changes were made since the newest commit.
$ git commit -m “my first commit”

$ git add example_file

$ git commit --amend
In the above example, a forgotten file is added to a commit.
Unstaging a File
$ git reset HEAD index.html

Unstaged changes after reset:

M index.html
Above, we see that the git reset HEAD command unstaged the index.html file.
 
NOTE: When git reset --hard is used, Git overwrites all changes in the working directory, permanently destroying any uncommitted changes.
Undo a Committed Snapshot
To undo changes resulting from a particular commit, use the git revert command. This command appends a new commit that undoes changes introduced by a specific commit. This prevents Git from losing history.
$ git commit -m "Example Commit"

$ git revert HEAD
*In the example above, a new commit gets appended and rolls back changes from a specific commit.
Unmodifying a File
To have a file return to its state when you last committed, utilize the git checkout command.
Example:
$ git checkout -- index.html
 
NOTE: git checkout -- file erases any changes made to the file because you are copying another file over it. Almost all committed information in Git can be recovered; however, any uncommitted information can be lost forever.
Branching
Almost every type of Version Control System incorporates branching. By creating branches of a central repository, collaborators are able to work on a project simultaneously via multiple branches, without affecting this main repository.
A collaborator can create a branch, work on it and save commit snapshots within it, switch between various branches, and merge changes. A Git branch is basically a movable pointer that always points to the most recent commit, or snapshot. Git uses the default local branch name “master,” which can be changed. Just because the default name is “master” does not imply that it is higher in importance or has more functionality than other branches. The head is a special pointer which indicates which branch you are currently working within.
 
Creating a New Branch
To create a new branch, use the git branch name format:
$ git branch test
*The above command creates a new branch named “test” that points toward your most recent commit. However, this command does not switch you over to this new branch.
 
Switching Branches
To switch to another branch, use the git checkout command.
$ git checkout test
*This command moves the HEAD pointer to the test branch
 
If you make a commit while on the test branch, only this branch will point to the most recent commit. The master branch will still point at the commit it was pointing to when you checked out to the test branch. So, if you switch back to the master branch, none of your recent changes made on the test branch will exist on the master branch.
Create a Branch and Checkout
To simultaneously create a new branch and switch to it, use the -b switch with the git checkout command:
$ git checkout -b test2
*The command above creates a new branch “test2” and switches you to it.
List Branches
You can list available branches by using the git branch command.
$ git branch

*master
Above, we see that we have one local branch, named “master”.
Merging
When you want to merge changes from one branch into your current one, you can use the git merge command.
Fast-Forward Merging
With a fast-forward merge, your current branch’s pointer moves forward to the most recent commit for the branch being merged in – there is no divergent work to merge together because the latter branch is directly upstream in relation to the former one.
Example:
$ git checkout master (switches you to the master branch)

$ git merge test (merges in changes from test branch)

Updating c58d775 .. 8b9205d

Fast-forward

index.html| 4 ++

1 file changed, 4 insertions(+)
 
In the diagram above, the Master branch, which previously pointed at Commit 3, now points at Commit 4, after fast forwarding and merging in changes from the Test branch – made possible by the fact that Master had not diverged from the latter.
No Fast-forward
When you use the git merge --no-ff <branch> command, instead of a branch simply moving its pointer forward, a new commit object is created. The –no-ff flag is often used to prevent the loss of historical information regarding a merged-in branch.
$ git merge test --no-ff
Three-way Merge
In cases of branches diverging, fast-forward merges are not an option. A three-way merge can be used, however. This type of merge involves the two latest commit snapshots pointed to by both branches, and their common ancestor. Here is an example of creating a three-way merge:
$ git checkout master

$ git merge test
 
Instead of just moving the branch pointer forward, Git creates a new snapshot that results from this three-way merge and automatically creates a new commit that points to it. This is referred to as a merge commit, which is special because it has more than one parent.
Fetch and Merge
To easily fetch and merge remote changes, use the git pull command in your working directory.
Deleting Branches
After you’ve merged branches, and they’re no longer needed, you can easily delete them with the -d flag.
Example:
$ git branch -d test
*This deletes the “test” branch.
Merge Conflicts
When the two files being merged both have changes in identical sections of a file, Git will not be able to complete the merge cleanly. These conflicts must be dealt with manually. Portions of files with unresolved merge conflicts will be labeled “unmerged”.
You can easily locate areas of merge conflict via Git’s conflict resolution markers, which appear in applicable files.
Example:
My name is

 <<<<<<< HEAD

 Jane

 =======

 Mary

 >>>>>>> branch-test
Here, HEAD indicates the branch you checked out before running the merge command. The content above the ======= resides within this branch, while everything below it is within the test branch. As you can see, the conflict is that Jane and Mary conflict with each other. After fixing this conflict and removing the ======= and >>>>>>> lines, run the git add command on fixed files to mark them as resolved.
To view unmerged files, use the git status command.
$ git status
# On branch master
# Unmerged paths:
# (use “git add/rm …” as appropriate to mark resolution)
#
# both modified: index.html
#
*Here, we see that there is a merge conflict in index.html.
Preview Changes
To preview changes for merging, use the git diff command in the following format:
git diff <source_branch> <target_branch>
Listing Branches
To list local branches, use the git branch command. The branch currently being worked on will have an asterisk next to its name.


