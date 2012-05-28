Markup README
=============

###### Copyright &copy; 2012 Mark Constable, License: [AGPLv3]

This simple project is a single file HTML5/CSS3 [Markup] page
that provides a minimal editor and [Markdown] preview system with
a few interesting features:

* a single self contained ~12KB page, just wget or copy [index.html]
* only depends are [marked.js] from Github, README.md, favicon.ico
* minimal modern HTML5/CSS3 page template for any purpose
* an ultra simple AJAX GET function that does not require jQuery
* example of including marked.js directly from its Github repo
* example [live site] taking advantage of Githubs gh-pages branch
* example of using localStorage() to store the editor contents
* example of using [QtCreator] generic project files
* dynamic CSS page resize using only `body {font-size: xxx%;}`
* won't work with older versions of IE (yes, that's a feature)

To see the page resize in action: use F12 in Chrome(ium) or
Firefox (assuming Firebug is installed) and select the `<body>`
tag then look for the `font-size: 100%` setting, click on it, and
change it anywhere from `50%` to `500%` and note how every element
on the page auto resizes accordingly.

Usage
-----

#### HELP
[Markdown] format help. Copy and paste sections into the editor to
see how the Markdown examples look when rendered into HTML

#### EDIT
Shows a simple plain textarea editor, add any valid markdown text
and click SHOW to see it marked up

#### SHOW
Shows the marked up HTML version of whatever is in the editor

#### HTML
Shows the raw HTML version of the marked up text

#### JSON
Shows the intermediate `Json` format from [marked.js]

#### STORE
Stores whatever is in the editor to localStorage so that a full
page refresh still contains the last edits

#### CLEAR
Clears the localStorage facility

#### README
Shows and marks up any README.md in the same folder as index.html,
compare to the original [Github GFM] [Markup]

#### SOURCE
The Github based source project


How To Setup Github Project Pages
---------------------------------

[pages.github.com] describes how to set up a Github managed
website for both users and projects. Here we will focus on how to
set up a **project site** using this project as a guiding example
where the master branch contains only files intended for the
gh-pages website. In this case our web files are already managed
in the master branch so we just want a gh-pages branch to mirror
the master branch in a way that we don't have to manually merge
our changes from the master branch to the gh-pages branch.

    PROJECT=    # your Github project name
    USERNAME=   # your Github user name
    cd ~/Devel  # your work area
    git clone git@github.com:$USERNAME/$PROJECT.git
    git branch --set-upstream gh-pages origin/master
    git push origin gh-pages

This makes a local clone of our remote Github project then
creates a gh-pages branch to mirror the remote origin master
branch and pushes that branch through to Github where in about 10
minutes the contents of the gh-pages branch will appear at...

    $USERNAME.github.com/$PROJECT

Now when we make local changes to these files we still need to
manually pull and push the gh-pages branch but at least we don't
have to mess around with local merging and manual editing in the
gh-pages branch.

    # example: update README.md
    git commit -am "Updated README.md"
    git push
    git checkout gh-pages
    git pull
    git push
    git checkout master

Remember to always switch back to the master branch to make
changes so the above just becomes a slightly tedious but trouble
free procedure. You can always set up shell alias to simplfy this
procedure and in this example below the first `git push` stage
will pull up your configured editor (ie; echo $EDITOR) to add the
commit message...

    alias gh='\
      git commit -a && \
      git push && \
      git checkout gh-pages && \
      git pull && \
      git push && \
      git checkout master'

Of course managing this repo via QtCreator will still require
manual mouse twiddling unless the above is converted to an
external command and used via `Tools -> External`. Using QtCreator
to save changes and then `Tools -> Git -> Commit` to provide the
commit message is reasonable so an external command to just manage
the push and pull actions is all that is needed...

    alias se='sudo nano -t -x -c'
    se /usr/bin/gh-pages

        #!/bin/sh
        git push && \
          git checkout gh-pages && \
          git pull && \
          git push && \
          git checkout master

    sudo chmod +x /usr/bin/gh-pages

and now link the above script to a Tools -> External menu option...

    Tools -> External -> Configure
    Add Category (ie; Git)
    Add Tool (ie; "Github Pages" under Git)
    Executable: gh-pages
    Working Directory: %{CurrentDocument:Path}

After making changes and adding a commit message just use...

    Tools -> External -> Git -> Github Pages
    instead of
    Tools -> Git -> Push (... and the other steps)

Now we have a truly cross-platform and totally free GUI programmers
editor and version controlled website (or code) management system.

[AGPLv3]: http://www.gnu.org/licenses/agpl.html
[Showdown]: https://github.com/coreyti/showdown
[Markdown]: http://daringfireball.net/projects/markdown
[index.html]: http://markc.github.com/markup/index.html
[pages.github.com]: http://pages.github.com
[marked.js]: https://github.com/chjj/marked
[Markup]: http://github.com/markc/markup
[live site]: http://markc.github.com/markup
[QtCreator]: http://qt-project.org/wiki/Qt_Creator_Releases
[Github GFM]: http://github.github.com/github-flavored-markdown/
