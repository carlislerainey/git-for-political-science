# How I Use Git and GitHub for Political Science Research

> Much like James Cameron's *Avatar*, Git doesn't make any goddamn sense. - [Zach Holman](http://zachholman.com/talk/more-git-and-github-secrets/) (starting at 1:43)

Git/GitHub is hard, and my experience aligns well with Zach's.

In spite of this, another Zach, [Zach Jones](http://zmjones.com/), [convinced](http://zmjones.com/git/) me to use Git/GitHub to publicly version-control my research projects with his [article](http://zmjones.com/git/) in *The Political Methodologist*. 

I had no trouble installing Git, setting up a GitHub account, initializing, adding, committing, and pushing. But I had a lot of questions. Many of these question did not revolve around the software, but around best practices.

* How often should I commit changes?
* Are commit messages important? Should I write one-liners or longer messages?
* What files should I track? Should I track the data? The manuscript?
* Given that I am not writing and releasing different versions of software, how should I use tags?
* How should a structure my files and directories to to get the most out of the process?
* What about coauthoring? 

In short, most users of Git/GitHub are programmers. I am a political scientist. Most users want to track software. I want to track an empirical research project (changes to the data, code, and manuscript). I had a lot of difficulty mapping the Git/GitHub facilities onto my needs as a researcher. I suggested the Zach write a guide for people like me. He told me:

> Git is a really complex piece of software. It isn't hard to learn how to do basic things, but introductions are probably better left to people who really understand things.

He's probably right, but I've poked around the Internet and can't find a useful introduction to GitHub for political scientists. For example, I'd like to have my graduate students publicly version control their research projects this fall, but I can't find a good introduction to Git/GitHub that suits their need. So I, the least qualified (well, probably not the least, but you know what I mean) among us, have decided to put my notes and thoughts about Git/GitHub on GitHub. I'm doing that with all my projects these days and I have found it well worth the effort. 

I'm certain that I could be doing things better. There are probably things that are just plain wrong. If you see things that I could do better or should do differently, please [open an issue](https://github.com/carlislerainey/git-for-political-science/issues?state=open), [email me](mailto:carlislerainey@gmail.com) or, even better, [fork the repository](https://github.com/carlislerainey/git-for-political-science/fork) and suggest a change. Part of my motivation in all of this is to learn something from the community of GitHub users in political science. Perhaps I have something to offer as well. 

There are several popular resources for learning Git and/or GitHub. Here are a few that I've found useful:
* An easy introduction to [setting up a repository](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1) and [basic Git functions](http://readwrite.com/2013/10/02/github-for-beginners-part-2).
* [Pro-Git](http://git-scm.com/book)
* [Try Git](https://try.github.io/levels/1/challenges/1)
* A [Git/GitHub Tutorial](http://kbroman.github.io/github_tutorial/), the [Most Important Git Commands](https://github.com/kbroman/Tools4RR/blob/master/04_Git/GitCommands/git_notes.md), and some [slides](http://kbroman.github.io/Tools4RR/assets/lectures/04_git_withnotes.pdf) from Karl Broman
* [GitHub Help](https://help.github.com/) pages
* Roger Dudler's [Simple Guide](http://rogerdudler.github.io/git-guide/)
* Some [slides](http://karthik.github.io/git_intro/#/slide-title) and a [paper](https://github.com/karthik/smb_git) from Karthik Ram
* An [introduction](http://nicercode.github.io/git/) from NiceRCode.

##  Motivation for Git Combined with GitHub.

* **Reproducibility**. The ability of others to reproduce your results is crucial to scientific credibility. By "reproducible," I simply mean that other researchers can take the original (raw) data and use the same techniques to generate your results. If this minimal standard is not met, then your research is simply not credible. Too often, "replication files" contain the final, cleaned data set and the script to run the final model. In my opinion, this does not meet the minimal standard and is an inefficient way for science to proceed. Publicly version-controlled research makes the *entire* project available to other researchers. That includes all the data (original, raw, messy data and cleaned versions), all the code (including code to do the data cleaning), and all the text produced as part of writing the manuscript. 
* **History.** We all use some form of version control. Most of us do it poorly. Using Git/GitHub, I'm learning to do it better. Git/GitHub offers a formal way to easily maintain a complete history of a project. In general, it's good to avoid filenames like `new_final_carlisle_v3c_updated.docx`. A recent [comic](http://www.phdcomics.com/comics/archive.php?comicid=1531) makes this point clear. Scott Clifford's [tweet](https://mobile.twitter.com/scotta_clifford/status/411610584468058112) rings so true--we need a method of updating files while keeping track of the old versions so that we can go back if needed. But the approach of giving different filenames to different versions is inefficient at best. My approach of keeping "old files" in a designated folder is no better. Git solves these issues. Second, Git allows you to tag a project at certain stages, such as "initial submission to AJPS." After getting an invitation to revise and resubmit and making the required changes, I can compare the current version of the project to the (now several months old) version I initially submitted. This makes writing response memos much easier.
* **Transparency.** Zach Jones most clearly [makes](http://zmjones.com/git/) the point that Git/GitHub increases transparency in the context of political science research. Git/GitHub essentially functions as an "[open notebook](http://en.wikipedia.org/wiki/Open_notebook_science)," allowing others to actively monitor the progress of a project or study its previous development. [Carl Boettiger](http://www.carlboettiger.info/lab-notebook.html) is [one](http://www.nature.com/naturejobs/science/articles/10.1038/nj7434-711a) of the most well-know proponents of open notebooks. This kind of openness provides a wonderful opportunity to receive comments and suggestions from a wide audience. This allows other to [catch errors](https://github.com/zmjones/eeesr/issues/1) that might otherwise go unnoticed. It also gives readers a formal avenue to [make suggestions](https://github.com/karthik/smb_git/issues?state=open), not to mention keeping a complete history of the suggestions and any subsequent discussion.
* **Accessibility.** Christopher Gandrud [makes](http://polmeth.wustl.edu/methodologist/tpm_v20_n2.pdf#page7) the point clearly in a recent edition of *The Political Methodologist*, though he discusses accessibility purely in the context of building data sets. But similar arguments could be made for code. I recently had a graduate student express interest in some MRP estimates of state-level opinion on the Affordable Care Act. I told her that I had spent some time collecting [surveys](https://github.com/carlislerainey/ACA_Opinion/tree/master/Data/Cleaned_Poll_Data) and writing [code](https://github.com/carlislerainey/ACA_Opinion/tree/master/R_Code) to produce the [estimates](https://github.com/carlislerainey/ACA_Opinion/blob/master/Data/mrp_est.csv). I noted that, ideally, she would not duplicate my work, but, if possible, build on it. I was able to point her to the [GitHub repository](https://github.com/carlislerainey/ACA_Opinion) for the project, which hopefully she'll find useful as a starting point for her own work. As part of my experience supervising replication projects as part of graduate methods classes and my own experience with replication data, the clean, final versions of the data that researchers typically post publicly do not allow future researchers to build on easily build on previous work. If authors posted the raw data and all the (possibly long and messy) code to do the cleaning and recoding, it would be much easier for future researcher to build on past contribution. Indeed, [research](http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0000308) shows that making the data and code freely available lowers the barriers to reuse and increases citations.

Thoughts from others on Git/GitHub.

* Karl Broman [likes](http://kbroman.github.io/github_tutorial/pages/why.html) Git/GitHub for its version control, easy merging, and openness.
* Karthik Ram [provides](http://www.scfbm.org/content/pdf/1751-0473-8-7.pdf) a very thorough discussion of the motivation for Git/GitHub in the context of scientific research.  Appropriately, there is a GitHub [repository](https://github.com/karthik/smb_git) for this paper. If you click over to the issues and/or history of this project, you can get a good feel for how this project benefitted from public version control.
* Carly Strasser [offers](http://datapub.cdlib.org/2014/05/05/github-a-primer-for-researchers/) a nice discussion of the benefits of Git/GitHub, including the idea of a "lab notebook."

## Some General Principles

The project directory should contain all the code, data, and text relevant to a particular project. I keep files that are not project-specific (e.g., research papers that I'm reading) in a separate directory. (I'm still deciding whether it makes the most sense to have a single "master" bibliography `.bib` file or a smaller `.bib` file for each project. I've done it both ways and both have strengths.) In order to effectively use version control, then the main files must be in plain text, such as `.R` scripts, Stata `.do` files, LaTeX `.tex` files, or Markdown `.md` files, or comma-separated `.csv` data files. The directory should be named something short and descriptive and should not contain spaces (such as `unreliable`, `Need`, or `strategic-mobilization`). In the past, I've used upper-case and underscores for directories, but I'm changing because a majority seem to use lower-case and dashes (it looks a little neater in GitHub). Rich Fitzjohn [provides](http://nicercode.github.io/blog/2013-04-05-projects/) a nice overview of *one* good way to layout your project directories. See also [this discussion](https://github.com/carlislerainey/git-for-political-science/issues/1) with Brenton Kenkel.

While Git (in principle) can track changes to binary files (such as `.xlsx`, `.docx`, or `.pdf`), it works best with plain text files (`.csv`, `.md`, `.tex`, .do). This allows Git to not only keep track of the versions, but to highlight any changes across versions. Therefore, for public version control to be *most* effective, you should plan on using plain text files for your data, manuscript, and code. Most code (such as `.do` files for Stata or `.R` scripts for R) are already in plain text, so no change is required. It is easy to convert data from Stata's proprietary `.dta` format or Excel's binary (but open) `.xlsx` format to a comma-separated `.csv` format that is more open, transparent, and trackable. Manuscripts present the biggest obstacle since switching from Microsoft Word's `.doc` or `.docx` formats to Markdown's `.md` or LaTeX's `.tex` is not trivial. However, this should not be a sticking point. When I coauthor with others who prefer Word, I simply track the `.docx` file. It is difficult to compare across different versions, but with descriptive commit messages and appropriate tagging at various stages of the publication process, Git works far better than `new_final_c_3b.docx`. If you are interested in using a more trackable format, then you can find more about `.tex` in the [wikibook](http://en.wikibooks.org/wiki/LaTeX) and `.md` (combined with `pandoc`) on John MacFarlane's [page](http://johnmacfarlane.net/pandoc/getting-started.html). You can find out more about the differences between these two from a [discussion](http://yihui.name/en/2013/10/markdown-or-latex/) by Yihui Xie.

## Install Git

Follow [these instructions](https://help.github.com/articles/set-up-git) to set up Git on your computer.

## Setup a GitHub Account

To setup a GitHub account, you simply need to go to [github.com/join](https://github.com/join), and provide a username, e-mail address, and password. You should choose your username carefully since it becomes an important part of your public profile. Shorter is better than longer, but you want people to associate it with you. I use "carlislerainey."

You might also want to setup an SSH key so that you don't need to provide your username and password when pushing to GitHub. While this is not necessary, it is convenient, so follow [these instructions](https://help.github.com/articles/generating-ssh-keys) to set it up.

## Setup a `.gitignore` File

By default, Git "suggests" tracking all files in a directory, but you'll want to always ignore some of these. For example, LaTeX generates a `.aux` file with each compiling, and there is no reason to track these. You'd like Git to ignore this file and others like it. You can do this easily by setting up a global `.gitignore` file. The manual [provides](http://git-scm.com/docs/gitignore) some useful information for setting this up.

The GitHub user octocat [provides](https://gist.github.com/octocat/9257657) a suggested set of files to ignore.

I tend to include a local`.gitignore` file so that I can easily control exactly what files are ignored within particular projects. That allows me to adjust to slightly different file structures or avoid tracking large data set or sensitive data. A basic template seems to work pretty well for me, so I'm including it below. 

    # ignore temp files w/ trailing ~
    *~

    # ignore hidden files
    .*
    
    # ignore files with the rolling extensions
    *.DS_Store
    *.Rhistory
    *.aux
    *.bbl
    *.blg
    *.log
    *.out
    *.toc
    *.synctex.gz
    *.bib.bak
    
    # ignore my old files
    old-files*
    
    # don't ignore the .gitignore file
    !.gitignore
    

Notice that I keep an `old-files` directory in each project directory, where I throw old files that I don't plan on using any more. This shows that I don't completely trust the version control system. I'll be rid of this soon.

I think it is a good idea to keep track of the `.pdf` of the manuscript. That makes it a little easier to inspect changes sometimes. Also, I think it is a good idea to track any R output, such as cleaned data set and figures, except when these are prohibitively large. (GitHub [limits](https://help.github.com/articles/what-is-my-disk-quota) users to 100MB per file and 1GB per repository.)

## Start Publicly Tracking a Project

1. **Create the README**. Start a file called `README.md` in the main directory. For now, this should be a short description of the project. As the project grows, this file can grow with it. I suggest linking to the relevant project files here (working papers, presentation slides, etc.) at the top of the README. This file should be a plain text document written in Markdown. If you're not familiar with the Markddown syntax, you can find out how to use it in about five minutes [here](http://daringfireball.net/projects/markdown/syntax), [here](), or [here]().
2. **Initiate .git**. Once you've started the README, you'll want to initiate .git version control within the project directory. To do this, simply open up a terminal, set the current directory to the project folder, and type the command `git init`. Now you're ready to publicly track your projects.

  In my case, I keep my projects inside a "Project" directory in a Dropbox folder that is common across all my computers (and my iPhone and iPad). To initiate tracking, I need to do the following in the terminal (on Mac OS X).

        cd ~/Dropbox/projects/strategic-mobilization
        git init

3. **Add the files you want to track.** To start tracking files, you first need to make sure that you are working in the project directory. Then you can use the command `git status` to see what files you are already tracking, if any. Then you can add files with the `git add` command. At first, I recommend adding files one at a time. For example, suppose that your project directory is called `strategic-mobilization`, and that the file you want to add, `stratmob.tex`, is located in the subdirectory `doc`. Then the following is what you want.

        git status
        git add doc/stratmob.tex
        git commit -m "add manuscript"

4. **Push your directory to GitHub.** Go to your GitHub page (i.e., https://github.com/username), click the "Repositories" tab, and click the "New" button. Give the repository a name. I always use the name of the project directory, but Brenton Kenkel and I had a useful [discussion](https://github.com/carlislerainey/git-for-political-science/issues/1) about this. Put in a short description of your project to help people find it (roughly less than 75 characters). GitHub will suggest that you several lines of code--don't run them yet.

There is a button near the top of the interface that allows you to switch from HTTPS to SSH. Just click it and GitHub will change its suggestion. Using SSH makes it easier to push commits to GitHub. It should look something like this.

    git remote add origin git@github.com:username/new_repo.git

Note: If you've set up the remote with the https://... url, then you can change it by simply removing the current remote by using `git remote rm origin` and then using the suggested alternative.

For more information, see Karl Broman's [discussion](http://kbroman.github.io/github_tutorial/pages/init.html) of initializing repositories.

## Update a Project

On thing that I first notice in my students, but now I see that I'm just as guilty of, is "the race to a regression." That is, I devote the absolute minimum required effort (or less) to everything leading up to the regression. My attitude is usually that I'll go back later and clean up everything, double checking along the way, if the line of investigation "proves useful" (i.e., provides stars). I rarely go back later. I find that my code that original was `let_me_just_try_this_really_quickly.R` becomes a part of `analysis.R`.

Instead of a race to the regression, Git encourages me to develop projects a little more carefully, thinking about projects in tiny steps, each to be publicly committed, and each done right.

In my view project development and Git/GitHub works best when users make small, discrete changes to a project. This takes some thought and discipline, but it is the best way to go. I'm guilty of coming back from a conference and making dozens of small changes to an existing projects, incorporating all the suggestions in a single update. I just [did it](https://github.com/carlislerainey/Need/commit/0b01f06df21926e784429b2221552a43bfc27912) after the State Politics and Policy Conference. This is a poor strategy, but I'm learning. It is a poor way to go about developing a project. It is a poor way to keep track of things. It is good to make small, discrete changes, and push those changes to GitHub.

To update a project, you need to do the following:

1. *Choose a discrete change to make to the project.* You need to describe the change in a sort commit message, so something like "add robustness check removing Alaska" or "rewrite the introduction" are good changes. If you notice something else to fix along the way, make a note of it and continue with your current update. Fix the other problem in a separate commit. It is extremely tempting to start fixing every problem you see. If you do this, you risk losing track of problems have been completely fixed, partial fixed, and need to be fixed later. A more deliberate, one-at-a-time approach is better.
2. *Make the change.* Do this just as you normally would. The only thing to avoid is moving or renaming files. Git has commands that take care of this and move the files' history with them (see below for more details).
3. *Stage the changes.* First, you should make sure that you are in the correct working directory. Then you should run `git status` and make sure that (1) you are on the correct branch (if you've started branching) and (2) that the modified files are as you expect. If everything is in order, then you need to add (or "stage") the modified files. I usually do this in one of three ways.
  1. Add files interactively. To do this, you can simply enter the command `git add -i` in the terminal. This causes Git to go into an interactive "shell mode" that allows you to select what you'd like to do (to add or "stage" files, choose update by typing "2" or "u" and pressing enter) and what files you'd like to do it to (type the number indexing the files you'd like to add, separated by commas, and press enter). Type "q" and press enter to quit the shell mode.
  2. Add the files manually. To do this, simply enter the command `git add folder/filename.ext`, with `folder` substituted with the directory of the modified file and `filename.ext` substituted with the appropriate filename and extension. With this approach you'll need to go through and add each modified file, one-at-a-time. Note that `git add folder` stages all the files and directories within `folder`, even those that were not previously tracked.
  3. Add all modified, previously tracked files. To do this, simply type `git add -u`. I find myself adopting this approach most often. I simple make sure that the files are modified as I expect by using `git status` beforehand.
4. *Commit the changes.* Once the modified files are staged, the changes need to be committed. To do this, simply enter the command `git commit -m "does this"`, where "does this" is replaced with a short, descriptive commit message. Writing a good commit message is important. Briefly, it should (in the present tense) briefly describe the changes made (e.g., "add education as control variable"). In my view, short commit messages work well for the type of commits that I typically make, but you should be aware that their are different perspectives. Some think that longer commit messages are important. To do a longer commit message, you'll want to [associate](https://help.github.com/articles/associating-text-editors-with-git) an editor with Git (I use the [vim](http://linux.startcom.org/docs/en/Introduction%20to%20Linux/sect_06_02.html) default for OS X) and use `git commit` which will open an editor and allow you to type a longer message as suggested [here](http://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message) [here](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html), [here](https://github.com/torvalds/linux/pull/17#issuecomment-5659933), [here](http://web-design-weekly.com/2013/09/01/a-better-git-commit/), and [here](http://zachholman.com/talk/more-git-and-github-secrets/) (starting at 15.24).
5. *Push the changes to GitHub.* Just type `git push` and the changes are sent off to GitHub so that the files are *publicly* version-controlled.

## Unstage a File

Suppose that you've staged a file to be committed, but now realize that the file shouldn't be included (i.e., it is a .aux file from LaTeX that you don't want to track, for example). You can unstage this file by entering the command `git reset HEAD path/to/file`. This unstages the file so that changes will not be committed as part of the next commit, but keeps any local changes.

## Move or Rename a File

If you want to move a file to a new location, you use the command below.

    git mv path/to/old/file.ext path/to/new/file.ext

To rename a file, the logic is nearly identical.

git mv path/to/old_filename.ext path/to/new_filename.ext

As long as you don't make any changes to the files being moved around or renamed, then Git will maintain the history of the file. If you make changes *and* move/rename the files, then you'll lose the history (i.e., Git thinks that this is a new file to be tracked).

## Using Tags Effectively

As far as I can tell, tags are intended to denote stable versions of software, such as version 2.0. However, I've found it useful to use tags to denote important versions of the project. For example, after I submit a manuscript to a journal, I tag the most recent commit with a descriptive label (e.g., `ajps-initial`) and short description (e.g., initial submission to AJPS). This makes it very easy to go back and compare the current version to the version initially submitted to the journal. This makes response memos a breeze.

### Assigning Tags

To assign a tag to the current commit, you just need to use 

    git tag -a descriptive-tag -m "short description" 

In practice, my tags look something like

    git tag -a jop-initial -m "initial submission to JOP"  

Importantly, after assigning the tag, you need to use `git push --tags` to push the tags to GitHub.

If you want to tag a previous commit, where `9fceb02` is first part of the commit ID, use

    git tag -a descriptive-tag 9fceb02 -m "short description"

You can use `git log` or explore the history of a project on GitHub to find the id of the desired commit. Notice that the ID is 40 characters long. It is enough to use just the first few.

If you want to change the name of a tag, use

    git tag new old
    git tag -d old
    git push origin :refs/tags/old
    git push --tags

### Comparing Tagged Versions

Once you are ready to compare the versions, you simply need to go use `git tag` to get a list of the tags for the project. If you prefer to work in the terminal, then you can just use `git diff -tag`, replacing "tag" with appropriate tag. However, I find it a little more useful to use the Compare View on GitHub ([here](https://github.com/github/linguist/compare/v2.2.0...v2.3.3)'s an example from GitHub). To do this, go to the project repository on GitHub and add `\compare` to the url. This brings up a compare window (more [here](https://github.com/blog/612-introducing-github-compare-view) and [here](https://help.github.com/articles/comparing-commits-across-time)). Click the dropdown menu for the base of comparison and type the name of the tag. Press enter and you have a nice summary of the differences between the tagged version and the current version of the project.

Note that if you are using binary files, such as `.docx`, you can download and compare the files yourself, but Git/GitHub will not highlight the differences as it will for plain text files such as `.md` or `.tex`.

Note that you can also view and explore the tagged versions of the project by clicking the "Releases" button on the GitHub repository page.

You can also compare the changes from tag1 to tag2 in `stratmob.tex` in the terminal `git diff`.

    GIT_PAGER='' git diff doc/stratmob.tex --color-words tag1 tag2

You can find out more about tagging from [Pro Git](http://git-scm.com/book/en/Git-Basics-Tagging).

## Make a Change to Someone Else's Project

Suppose you want to make a change to someone else's project. It might be that you are making a change to a project hosted by a coauthor or want to make a suggested change to a total stranger's code. The basic idea is to fork their repository into your own GitHub account, clone it onto your hard drive, make any changes, and submit a pull request.

## Misc. Material

A nice [comic](http://www.osnews.com/story/19266/WTFs_m) on high-quality code.
