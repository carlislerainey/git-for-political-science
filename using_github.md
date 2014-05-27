# How I Use Git and GitHub for Political Science Research

[Zach Jones](http://zmjones.com/) prompted me to use Git/GitHub with his [article](http://zmjones.com/git/) in *The Political Methodologist*. I'm not a programmer, but I'm probably above the median in my tech-savyness. Git/GitHub was hard for me to learn. I had no trouble, installing Git, setting up a GitHub account, initializing, adding, committing, and pushing. But I had a lot of questions. Many of these question did not revolve around the software, but around best practices.

* How often should should I commit changes?
* What files should I track? Should I track the data? The manuscript?
* Given that I am not writing and releasing different versions software, should I be using tags?

In short, most users of Git/GitHub are programmers. I am a political scientist. Most users are tracking software. I want to track an empirical research project. I had a lot of difficulty mapping the Git/GitHub facilities onto my needs as a researcher. I suggested the Zach write a guide for people like me. He told me:

> Git is a really complex piece of software. It isn't hard to learn how to do basic things, but introductions are probably better left to people who really understand things.

Well, I've poked around the Internet and can't find a useful introduction to GitHub for political scientists. For example, I'd like to have my graduate students publicly version control their research projects this fall, but I can't find a good introduction to Git/GitHub that suits their need.

So what I've decided to do is put together all the useful links and snippets of code that I've found useful and describe how I've incorporated it into my workflow. I'm certain that I could be doing things better. There are probably things that are just plain wrong. If you see things that I could do better or should do differently, please create an issue or, even better, fork the repository and suggest a change.

There are several popular resources for learning Git and/or GitHub. Here are a few that I've found useful:

* [Pro-Git](http://git-scm.com/book)
* [Try Git](https://try.github.io/levels/1/challenges/1)
* A [Git/GitHub Tutorial](http://kbroman.github.io/github_tutorial/), the [Most Important Git Commands](https://github.com/kbroman/Tools4RR/blob/master/04_Git/GitCommands/git_notes.md), and some [slides](Karl Broman) from Karl Broman
* [GitHub Help](https://help.github.com/) pages
* Roger Dudler's [Simple Guide](http://rogerdudler.github.io/git-guide/)
* Some [slides](http://karthik.github.io/git_intro/#/slide-title) and a [paper](https://github.com/karthik/smb_git) from Karthik Ram
* An [introduction](http://nicercode.github.io/git/) from NiceRCode.

##  Motivation for Git Combined with GitHub.

* **History.** We all use some form of version control. Most of us do it poorly. Using Git/GitHub, I'm learning to do it better. Git/GitHub offers a formal way to easily maintain a complete history of a project. In general, it's good to avoid filenames like `new_final_carlisle_v3c_updated.docx`. A recent [comic](http://www.phdcomics.com/comics/archive.php?comicid=1531) makes this point clear. Scott Clifford's [tweet](https://mobile.twitter.com/scotta_clifford/status/411610584468058112) rings so true--we need a method of updating files while keeping track of the old versions so that we can go back if needed. But the approach of giving different filenames to different version is inefficient at best. My approach of keeping "old files" in a designated folder is no better. Git/GitHub solves these issues. Second, Git allows you to tag a project at certain stages, such as "Initial submission to AJPS." After getting an invitation to revise and resubmit and making the required changes, I can compare the current version of the project to the (now several months old) version I initially submitted. This makes writing response memos much easier.
* **Transparency.** Zach Jones most clearly [makes](http://zmjones.com/git/) the point that Git/GitHub increases transparency in the context of political science research. Git/GitHub essentially functions as an "open lab notebook" allowing others to actively monitor the progress of a project or study its previous development. Related to the motivation to using GitHub in an open manner is the [idea](http://www.nature.com/naturejobs/science/articles/10.1038/nj7493-523a) of an "[open notebook](http://en.wikipedia.org/wiki/Open_notebook_science)." [Carl Boettiger](http://www.carlboettiger.info/lab-notebook.html) is [one](http://www.nature.com/naturejobs/science/articles/10.1038/nj7434-711a) of the most well-know proponents of open notebooks. This kind of openness provides a wonderful opportunity to receive comments and suggestions from a wide audience. This allows other to [catch errors](https://github.com/zmjones/eeesr/issues/1) that might otherwise go unnoticed. It also gives readers a formal avenue to [make suggestions](https://github.com/karthik/smb_git/issues?state=open), not to mention keeping a complete history of the suggestions and any subsequent discussion.
* **Accessibility.** Christopher Gandrud [makes](http://polmeth.wustl.edu/methodologist/tpm_v20_n2.pdf#page7) the point clearly in a clearly in a recent edition of *The Political Methodologist*, though he discusses accessibility purely in the context of building data sets. But similar arguments could be made for code. I recently had a graduate student express interest in some MRP estimates of state-level opinion on the Affordable Care Act. I told her that I had spent some time collecting [surveys](https://github.com/carlislerainey/ACA_Opinion/tree/master/Data/Cleaned_Poll_Data) and writing [code](https://github.com/carlislerainey/ACA_Opinion/tree/master/R_Code) to produce the [estimates](https://github.com/carlislerainey/ACA_Opinion/blob/master/Data/mrp_est.csv). I noted that, ideally, she would not duplicate my work, but, if possible, build on it. I was able to point her to the [GitHub repository](https://github.com/carlislerainey/ACA_Opinion) for the project, which hopefully she'll find useful as a starting point for her own work. As part of my experience supervising replication projects as part of graduate methods classes and my own experience with replication data, the clean, final versions of the data that researchers typically post publicly do not allow future researchers to build on easily build on previous work. If authors posted the raw data and all the (possibly long and messy) code to do the cleaning and recoding, it would be much easier for future researcher to build on past contribution. Indeed, [research](http://www.plosone.org/article/info%3Adoi%2F10.1371%2Fjournal.pone.0000308) shows that making the data and code freely available lowers the barriers to reuse and increases citations.

Thoughts from others on Git/GitHub.

* Karl Broman [likes](http://kbroman.github.io/github_tutorial/pages/why.html) Git/GitHub for its version control, easy merging, and openness.
* Karthik Ram [provides](http://www.scfbm.org/content/pdf/1751-0473-8-7.pdf) a very thorough discussion of the motivation for Git/GitHub in the context of scientific research.  Appropriately, there is a GitHub [repository](https://github.com/karthik/smb_git) for this paper. If you click over to the issues and/or history of this project, you can get a good feel for how this project benefitted from public version control.
* Carly Strasser [offers](http://datapub.cdlib.org/2014/05/05/github-a-primer-for-researchers/) a nice discussion of the benefits of Git/GitHub, including the idea of a "lab notebook."


## Some General Principles

1. The project directory should contain all the code, data, and text relevant to a particular project. I keep files that are not project-specific (e.g., papers and bibliography information in separate directories.) In order to effectively use version control, then the main files must be in plain text, such as .R scripts, Stata .do files, LaTeX .tex files, or Markdown .md files, or comma-separated .csv data files. The directory should be named something short and descriptive and should not contain spaces (such as NME, Need, or ACA_Opinion). Note that I capitalize directories and use lower-case for files, but a majority seem to use lower-case always. Rich fitzjohn [provides](http://nicercode.github.io/blog/2013-04-05-projects/) a nice overview of *one* good way to layout your project directories.

## Install Git

Follow [these instructions](https://help.github.com/articles/set-up-git) to set up Git on your computer. 

## Setup a GitHub Account

You might also want to setup an SSH key so that you don't need to provide your username and password when pushing to GitHub. While this is not necessary, it is convenient, so follow [these instructions](https://help.github.com/articles/generating-ssh-keys) to set it up. 

## Setup a `.gitignore` File



## Start Publicly Tracking a Project 

1. **Create the README**. Start a file called `README.md` in the main directory. For now, this should be a short description of the project. As the project grows, this file can grow with it. I suggest linking to the relevant project files here (working papers, presentation slides, etc.) at the top of the README. This file should be a plain text document written in Markdown. If you're not familiar with the Markddown syntax, you can find out how to use it in about five minutes [here](http://daringfireball.net/projects/markdown/syntax), [here](), or [here]().
2. **Initiate .git**. Once you've started the README, you'll want to initiate .git version control within the project directory. To do this, simply open up a terminal, set the current directory to the project folder, and type the command `git init`. Now you're ready to publicly track your projects.
3. **Push your directory to GitHub.** Go to your GitHub page (i.e., https://github.com/username), click the "Repositories" tab, and click the "New" button. Give the repository a name--I always use the name of the project directory. 

## Update a Project

I should add something about the race to a regression here.

In my view project development and Git/GitHub works best when users make small, discrete changes to a project. This takes some thought and discipline, but it is the best way to go. I'm guilty of coming back from a conference and making dozens of small changes to an existing projects, incorporating all the suggestions in a single update. This is a poor strategy. It is a poor way to go about developing a project. It is a poor way to keep track of things. It is good to make small, discrete changes, and push those changes to GitHub.

## Make a Change to Someone Else's Project 

Suppose you want to make a change to someone else's project. It might be that you are making a change to a project hosted by a coauthor or want to make a suggested change to a total stranger's code. The basic idea is to fork their repository into your own GitHub account, clone it onto your hard drive, make any changes, and submit a pull request. 

## Misc. Material

[Writing Good Commit Messages](https://github.com/erlang/otp/wiki/Writing-good-commit-messages)

[Here](http://who-t.blogspot.com/2009/12/on-commit-messages.html)'s more on committ messages.

A nice [comic](http://www.osnews.com/story/19266/WTFs_m) on high-quality code.