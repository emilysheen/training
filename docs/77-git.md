# Git

[Software-Carpentry Git Lesson][3]

DataCamp Courses:

- [Introduction to Git for Data Science][1]
- [Working with the RStudio IDE (Part 2) -- Chapter 2: Version Control][2]

Quick References:

1. [Software-Carpentry Reference][5]
2. [Git Cheat Sheet (by Github)][4]
3. [Jenny Bryan's "Happy Git and GitHub for the useR"][6]
4. [Git interaction from NDP Software][7]
5. [Learn Git Branching][8]

Git and the "final" version problem

If these comics bring back haunting memories, then version control is for you!

![](http://www.phdcomics.com/comics/archive/phd101212s.gif)

![](http://www.phdcomics.com/comics/archive/phd052810s.gif)

Technically, renaming copies of files is a form of version control.
It allows you to go back to a specific state of a file.
As the two comics point out, this usually ends up in a cacophony of files with similar names.

What about files and programs that know how to track changes already.
I'm mainly thinking about Word documents.

## Git on your own

<div class="figure" style="text-align: center">
<img src="./figs/git_dspg2018-fellows-1.jpg" alt="Diagram of Git commands and how they relate to one another."  />
<p class="caption">(\#fig:unnamed-chunk-1)Diagram of Git commands and how they relate to one another.</p>
</div>

How not to write commit messages:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">how <a href="https://twitter.com/hashtag/not?src=hash&amp;ref_src=twsrc%5Etfw">#not</a> to write <a href="https://twitter.com/hashtag/git?src=hash&amp;ref_src=twsrc%5Etfw">#git</a> <a href="https://twitter.com/hashtag/commit?src=hash&amp;ref_src=twsrc%5Etfw">#commit</a> messages  -.-&#39;&#39; <a href="http://t.co/5TdiZ1yi5S">pic.twitter.com/5TdiZ1yi5S</a></p>&mdash; Dⓐniel Chen (@chendaniely) <a href="https://twitter.com/chendaniely/status/588826374208618496?ref_src=twsrc%5Etfw">April 16, 2015</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## Git with branches

<div class="figure" style="text-align: center">
<img src="./figs/git_dspg2018-fellows-self_review.jpg" alt="Review of Git"  />
<p class="caption">(\#fig:unnamed-chunk-2)Review of Git</p>
</div>

<div class="figure" style="text-align: center">
<img src="./figs/git_dspg2018-fellows-branching.jpg" alt="What branching looks like in the Git world"  />
<p class="caption">(\#fig:unnamed-chunk-3)What branching looks like in the Git world</p>
</div>

## Collaborating with Git

<div class="figure" style="text-align: center">
<img src="./figs/git_dspg2018-fellows-model_fork.jpg" alt="The 'forking' model of Git workflows"  />
<p class="caption">(\#fig:unnamed-chunk-4)The 'forking' model of Git workflows</p>
</div>

<div class="figure" style="text-align: center">
<img src="./figs/git_dspg2018-fellows-2.jpg" alt="Git with branches"  />
<p class="caption">(\#fig:unnamed-chunk-5)Git with branches</p>
</div>

## Protecting branches

https://docs.gitlab.com/ee/user/project/protected_branches.html

In a repository go to settings > repository > protected branches

set

- "allowed to merge": masters
- "allowed to push": no one


- If you accidently did work on `master`:

1. create a branch where you are now: `git branch BRANCH_NAME`
2. reset master to where you were: `git reset --hard COMMIT_HASH_FOR_MASTER`
    - make sure you do this on the `master` branch
3. go to your branch: `git checkout BRANCH_NAME`
4. push your branch: `git push origin BRANCH_NAME`
5. create and merge the pull/merge request

[1]: https://www.datacamp.com/courses/introduction-to-git-for-data-science
[2]: https://www.datacamp.com/courses/working-with-the-rstudio-ide-part-2
[3]: http://swcarpentry.github.io/git-novice/
[4]: https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf
[5]: http://swcarpentry.github.io/git-novice/reference/
[6]: http://happygitwithr.com/
[7]: http://ndpsoftware.com/git-cheatsheet.html
[8]: https://learngitbranching.js.org/
