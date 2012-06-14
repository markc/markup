Markup README
=============

###### Copyright &copy; 2012 Mark Constable, License: [AGPLv3]

This very simple project is mainly comprised of a [HTML5], [CSS3]
and [Javascript] single page interface ([SPI]) file that provides
an embedded [Markdown] editor and preview system. It's meant to be
used as a template for a new site but it is also somewhat useful
in its own right to edit and preview Markdown formatted text. It
can also store a working copy in [localStorage] so it's available
the next time you visit the page. Perhaps the most interesting
feature is how it can markup [Markdown] formatted text dynamically
within the browser. This [README.md] is an example of it doing
just that.

To summarize a few interesting features:

* a single self contained ~20KB page, just wget or copy [index.html]
* only external depends are [marked.js] and the [Open Sans] font
* minimal modern HTML5, CSS3 and JS page template for any purpose
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


[AGPLv3]: http://www.gnu.org/licenses/agpl.html
[Showdown]: https://github.com/coreyti/showdown
[Markdown]: http://daringfireball.net/projects/markdown
[index.html]: http://markc.github.com/markup/index.html
[pages.github.com]: http://pages.github.com
[marked.js]: https://github.com/chjj/marked
[Open Sans]: http://fonts.googleapis.com/css?family=Open+Sans:300
[Markup]: http://github.com/markc/markup
[live site]: http://markc.github.com/markup
[QtCreator]: http://qt-project.org/wiki/Qt_Creator_Releases
[Github GFM]: http://github.github.com/github-flavored-markdown/
[SPI]: http://en.wikipedia.org/wiki/Single-page_application
[HTML5]: http://en.wikipedia.org/wiki/HTML5
[CSS3]: http://en.wikipedia.org/wiki/CSS3#CSS_3
[Javascript]: http://en.wikipedia.org/wiki/Javascript
[README.md]: README.md
[localStorage]: http://en.wikipedia.org/wiki/LocalStorage
