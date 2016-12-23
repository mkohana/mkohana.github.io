+++
date = "2016-12-23T21:11:48+09:00"
title = "Open My Web Site"
math = false
tags = [
"hugo", "web site", "github", "github pages"
]
image = ""

+++

Today I open my web site.
This site is powered by [hugo](https://gohugo.io)
and uses [academic template](https://github.com/gcushen/hugo-academic)
created by George Cushen.
To host my site, I use github pages. However, I was faced with some problems.
The following is a note for me to host a hugo site on github pages.

### Repository Structure
The most web sites or blogs creates two branches, master and gh-pages.
The master branch includes the sources.
Using these source files, hugo builds a web site under the public directory
(that can be changed on config.toml).
The gh-pages branch has the site created by hugo
and it is published on github pages.

However, personal or organization github pages cannot use gh-pages branch.
On these github pages, the master branch is published as a web site.
Therefore, we need to push the files under the public directory
to the master branch.
So I create master branch and devel branch.
The deploy method follows [the official document](https://gohugo.io/tutorials/github-pages-blog/).
And I replace "master" with "devel" and also "gh-pages" with "master"

Finally, I had mistake on the config.toml.
If the "/" at the last of baseurl, the created link misses the separater.
As the result, the link target becomes "github.iopublication", for example.
