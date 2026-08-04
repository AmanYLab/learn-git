LearnGit:

Git is software and GitHub is a service.
 ( git --version to know the version of the git installed )
  									#To create a new folder using commando(Warp): mkdir nameofthefolder
 									#To create new file using commando (Warp) : New-Item Filename -ItemType File

Version control system :
it keeps the track of file

Rebo(Repository): a folder with a lot of software files

git helps to control a given file or folder . To use git in a given folder :
1) cd into the file,
2) ls to see the folder/file ,
3) check the git status ,
4) run git init to start the git version control system( Git Rebo).

What happened:
git init commando is ran once per folder. What it does is , it initialize and   creates a .git folder.

.git - is a hidden folder to keep history of all files and sub folder.
  ( to check the hidden forlder run " ls -la / ls -Force")

commit - check point(like game)

Write code - Add to git tracking zone - Commit:

			1.working Dir
			    >		git add  ( When we use this command , we are adding the file into git tracking zone)
			2.Staging Area
            
		             >  	git commit ( when committing any given file , it is must to add a message [ git commit -m ""]
						     to uncommit a file: we use [ git rm --cached <filename>] )

			3.Rebo
			     > 		git push
        	4.Github
hen committing a new file, message needs to be added. If not , it will take you a new page using your commando using Wrap vim/lingo.

 ### TO EXIT THIS PAGE  ->[PRESS ESC THEN WRITE :q!]

	
The whole step soo far ( Using a commando ):

			1 mkdir <foldername>                       - to create a folder
			2 git init                                 -to initialize Git
			3 New_Item <filename.txt>-ItemType File    - To create a new file inside a given folder
     		4 git add Filename.txt                     - to stage the file
			5 git commit -m"Message"                   - to commit the files
			6 git log or git log --oneline		    - to check the information about the commit
			7 git commit -am "text message"            - to add and commit as the same time

# Git Branch:  at first there is always a *Main branch , then user can add otherbranches using the commando [git branch <branch-name>]
After creating another branch: use [git checkout <branch-name>] to access the new branch.

# If a Master branch creates other branches that does other works , until they begin working seperatly , both branches of the master and new branch will be the same or have the same content , id etc...  . If one user uses the Master branch , the other branches work will be cleared by defualt and vise versa.


The HEAD alwasy points to where branch is currently at.

codes/commandos :                	# Commit before using/switching to another branch.
git branch                           - To check in which branch your at.
git branch bugfix                    - Created a new branch called bugfix.
git switch bugfix                    - To switch from the current branch to bugfix.
git log --oneline                    - To check the information about the branches
git switch master                    - To switch to the master branch 
git switch                           -c dark-mode ( create a branch and move there)
git checkout                         -b pink-mode
git merge bugfix                     - ( #Used in the below topic )


Branch merging:
	

Git diff [git diff] ( Informative command ) : shows the difference between The same file before staging and in/after staging . used as a comparison between before and after/in staging

# HOW TO READ DIFF:

a -> file1 and b -> File 2 ( Which file 2 is the changed version of file one )
--- file 1 and +++ file 2
* Changes in lines and little preview git

[git diff --staged] - shows use the comparison of the two version of the same file ( before and in/after staging ) . If 2 or more files are being checked inside the 'git diff --staged ' , it will show us both or all  version of files. * TO EXIT THE OBSERVATORY SECTION : PRESS Q*


Git stash [ git stash /git stash -u] : This code lets us switch branch's without committing our work. In git , one branch must commit there work before switch . 'git stash' allows use to switch these branches and comeback and maybe do more work or commit them.

# Stash is a temporary shield that you can use to store values and bring them back using :

[git stash pop] - is used to show the stashed files or changed after coming back to the same branch we 'git stash' before,


# MORE_COMMANDS:
git checkout <hash> - ( Detach head ) new branch
git switch master - (re-attach head)
git checkout HEAD -2 (look at 2 commit prior)
git restore filename (get back to last commit version )
git reflog (Moves the head into the original position, shows you the branchs and there Hash)



Git Rebase : * THIS COMMAND IS NOT SPOUSE TO BE RUN INSIDE THE MASTER/MAIN BRANCH*
 
               Can be used to merged alternative or branches or can be used  as a clean up tool.

[git rebase <branchname>] - this command is used to merge the branch mentioned to the branch your at .

when using the rebase command , There will be conflicts with the merging files or conflicted files that will be need to be solved manually.
After these conflicts are added , we then procced with the :
 							1. [ git add <conflicted-files> / git  add .] which is used to add the file
							2. [ git rebase --continue ] to finish the rebase process

#### NEVR REBASE COMMITS THAT YOU HAVE SHARED
#### NEVER REBASE PUSHED TO GIT HUB FILES


Git-Hub : A very famous online cloud service that can store repository . 
  Using git , we can create a repository and modify it , Now we can either create a new repo or publish the rebo we've been working on inside our terminal and vs-code . To do that:
		1. Generate a ssh-key 
		2. configure the key with the shh-agent 
		3. secure the .pub key inside the GitHub section

### Checkout the Gitdocs for more info https://docs.github.com/en

Git-Hub :
Git is a software and Git-Hub is a service to hose git repos online.
   .GitHub -> collaboration + backup + opensource 
Setups ssh key to connect with GitHub ,GitHub uses ssh to allow you to push code.

## Working in this repo file has four stages :
1.working stage - the stage after you initialize git and start working.
2.staging area - the stage after you add your work 
3.local Repo  - this stages comes after you committed your work 
4.Remote Repo - the stage after you push the file into GitHub.