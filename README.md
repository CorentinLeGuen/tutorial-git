# A simple tutorial

How to create a repository in GitHub and publish stuff ?

You can read the official documentation [here](https://git-scm.com/doc). And if you are on Windows, you can use this useful software : [GitForWindows](https://gitforwindows.org/).

![Get to know](https://cdn.scotch.io/1/school-start/web-dev-starter/get-to-know-git.png)

## Create a repository in GitHub

![GitHub repo](imgs/01.png)

Enter a name for your repository and a description :

![GitHub repo](imgs/02.png)

You can see the URL to access your repository :

![URL](imgs/03.png)

Push this button to copy in clipboard the URL automaticaly :

![COPY](imgs/04.png)

## Create a project in your computer

Create a repository in your computer and use ```git init .``` to initialize the project :

![Project in computer](imgs/05.png)
![Git init](imgs/06.png)

## Synchonize

Past the copied link to your git project to synchronize the distant GitHub repository with your local git repository :

![Synchro](imgs/07.png)

## Add work

Add a new file and commit your work :

![Add Readme](imgs/08.png)
![Commit](imgs/09.png)

You should create the distant branch *master* with :

![push -u](imgs/10.png)

The command ```git push -u <remote> <branch>``` is used to create a distant branch who didnt exist yet.

And you can see your work in GitHub ! **Congratulation!**

![Good Job](imgs/11.png)

Let's add another stuff !

![new file](imgs/12.png)

You can use ```git status``` to see what's new in your computer :

![new stuff](imgs/13.png)

And push your job :

![another push](imgs/14.png)

Use `git log` to see all commits :

![log](imgs/15.png)

## Create a new "branch"

A new branch is used to work with multiple coworkers or to "clean" the job. It's easier to see the "feature" of a coworker when he work on his own branch who's named "feature/fix-api-security" for example. And you will not realise simultaneous pushes that can destroy the git repository and result to a chaotic project.

![new branch](imgs/16.png)

Don't forget to ```push``` the local branch to create the distant branch with :

![push -u](imgs/20.png)

Then update or create new stuff :

![update](imgs/17.png)

When you have updated something, you can use ```git diff``` to see what have been modified :

![diff](imgs/23.png)

And push your work :

![status](imgs/18.png)
![commit](imgs/19.png)

## Amend a commit

When you have modified a file and you want to update it one more time without creating a new commit, you can use this command :

![oups](imgs/24.png)

Make the fix and :

![amend](imgs/27.png)

Don't forget to use `git push --force` after a commit.\
:warning: **Never use `amend` on a merge commit!**

## Merge

### In command line

To merge two branches, you can use `git merge <branch-name>` :

![merge](imgs/28.png)
![log](imgs/29.png)

### Directly on GitHub

This method is used when you work on team and you need to submit your job.

![add stuff](imgs/30.png)

Go to GitHub :

![pull](imgs/31.png)

Use "Compare & pull request" to submit your work :

![compare](imgs/32.png)

Add a commit name, a description. You can see on the bottom of the page the differences between the current branch (here *master*) and the submited branch.

![submit](imgs/34.png)

Then push "Create pull request" and GitHub will check if you have some conflicts before merging the branches :

![merge pull request](imgs/35.png)

And then you will see :

![well done](imgs/36.png)

![stuff merged](imgs/37.png)

## Conflicts

When someone push stuff on branch "A" and someone else push stuff on the same file on branch "B" and then branches are pull requested, you can see a merge conflict like this :

On branch master :
![push branch A](imgs/38.png)

On branch develop :
![push branch B](imgs/39.png)

And then merge on master :
![conflicts!](imgs/40.png)

Just use `git diff` to show where is the conflict and choose your modifications :

![diff conflict](imgs/41.png)

After remove the "======" and choose the apropriate modifications, you can use `git add` and `git merge --continue` to update the work :

![merge continue](imgs/42.png)

This simple tutorial is over, **congratulation**!

If you are reluctant to use the command line git, there is some softwares like [Sourcetree](https://www.sourcetreeapp.com/) or [GitKraken](https://www.gitkraken.com/). But I think there is nothing better than the good old command line !

For more informations, you can contact me on *leguen.corentin42@gmail.com*.