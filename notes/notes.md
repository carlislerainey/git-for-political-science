# Notes

This is just a collection of incomplete notes. It includes some links to idea I want to investigate further, some incomplete ideas that I want to incorporate into the main document, and some open questions that I have about best practices. 

## Avoiding Merge Conflicts

http://kernowsoul.com/blog/2012/06/20/4-ways-to-avoid-merge-commits-in-git/

## Motivation

I need to add a few lines about the way that git encourages you to slow down, keep things organized, and think in discrete steps.

## Setting, Updating, and Examining Remotes

`git remote`, `git remote -v`,  `git remote -va`

I once wanted to change the URI of the origin remote. I originally called the GitHub repository for this document `GitHub`, but Brendan Kenkel [suggested](https://github.com/carlislerainey/git-for-political-science/issues/1) that I rename it `git-for-political-science`. After using the GitHub interface to rename the repository, my remotes point to the old name.

    $ git remote -v
    origin ssh://git@github.com/carlislerainey/GitHub.git (fetch)
    origin ssh://git@github.com/carlislerainey/GitHub.git (push)

This is okay because GitHub will redirect my pushes, but I am a bit obsessive about these things, so I used 

    git remote set-url origin ssh://git@github.com/carlislerainey/git-for-political-science.git`

Now I have exactly what I want.

    $ git remote -v
    origin ssh://git@github.com/carlislerainey/git-for-political-science.git (fetch)
    origin ssh://git@github.com/carlislerainey/git-for-political-science.git (push)

## Collaborating

This [post](http://spring.io/blog/2010/12/21/social-coding-in-spring-projects) has a useful workflow, though not based on GitHub.

I think the most useful workflow seems to be the [forking workflow](https://www.atlassian.com/git/workflows#!workflow-forking), but there are other options there as well.

Open questions:

* Should each change be submitted as a separate branch? This [answer](http://stackoverflow.com/questions/8450036/how-to-open-multiple-pull-requests-on-github) has some bearing on the question. This [answer](http://stackoverflow.com/questions/7523557/submitting-multiple-pull-requests-in-git-with-github-general-flow) suggests that a pull request be one branch with several commits, each with its own descriptive commit message. But this [post](http://ellislab.com/blog/entry/contribution-guide) suggest one change per  pull request. Here's [another](http://codeinthehole.com/writing/pull-requests-and-other-good-practices-for-teams-using-github/) post that makes the same suggestion. 
* If so, should these branches be merged in locally before making new changes or should a new branch be started from master prior to merging? An [answer](http://stackoverflow.com/questions/16696528/how-to-submit-multiple-pull-requests-in-github-when-they-may-conflict-slightly) partly addresses this point.

As far as I can tell, there are three models for collaborating on GitHib.

1. Single change (with possibly multiple commits). Discussion. Another change. Dependent future changes must wait until after the discussion.
2. Multiple changes with multiple commits as part of a single pull request. This allows the requester to move on while the changes are being evaluated.
3. Allow the coathors to push directly to GitHub.

In order to collaborate with someone, it seems to make the most sense to follow the model of fork-clone-pull-branch-push-request.

1. *Fork.*
2. *Clone.* Refer to upstream remotes by your friend's username (see [here](http://blog.evan.pro/keeping-a-clean-github-fork-part-1)). Use `git remote -v` to see the current remotes.
3. *Pull*. Before you go any further, you probably want to make sure that you are working with the latest version of the repository, so use

    git pull --ff-only myfriend master

  The `git pull` command combines `git fetch` with `git merge` in a single two-step process. the `--ff-only` ensures that you only "fast-forward" to the latest version in your friend's `master` branch, where the remote `myfriend` point toward your friend's repository.

After pulling the latest version, you probably want to use `git push` to push any changes back up to your version on GitHub

4. *Branch.* If you don't branch, then you won't be able to separate your changes into reasonable sections.
5. *Push.* In general, use `git push origin new_feature` to push the branch new_feature to GitHub using the `origin` remote (`origin` is usually the remote you want). I prefer to have `git push` push the current branch by default. You can set this using 

    git config --global push.default current

  After running this configuration command, `git push` pushes the current branch to that branch's remote, which will be `origin` unless you've changed it. I think this makes `git push` work like `git push origin HEAD`, see [here](https://www.kernel.org/pub/software/scm/git/docs/git-push.html).

  For more details, see [here](http://stackoverflow.com/questions/948354/git-push-default-behavior).

6. *Pull Request*. After pushing the branch up to GitHub, you can login to GitHub, navigate to that branch and click submit pull request. 

7. *Merge*.