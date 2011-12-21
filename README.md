Markup README
=============

###### Copyright &copy; 2011 Mark Constable -- License: [AGPLv3]

This project was going to be my attempt at a modified and simpler
version of [Showdown], a Javascript port of the original perl based
[Markdown], but after a few days hacking and going around in circles
I discovered [marked] which is almost ideal for my needs and much
easier to modify, if need be. The project does include a single file
HTML5/CSS3 [MarkupTest] page that provides a minimal editor and markup
preview system with a few interesting features:

- a single self contained page, just wget [index.html]
- example of including marked.js directly from its Github repo
- example live site taking advantage of Githubs gh-pages branch
- minimal HTML5/CSS3 page template for any purpose
- an ultra simple AJAX GET function that does not require jQuery
- example of using localStorage() to save the editor contents
- example of using [QtCreator] generic project files
- dynamic CSS pagesize using `body {font-size: 100%;}`
- CSS3 rollover link "buttons" and body pagesize transition
- won't work with older versions of IE (yes, that's a feature)

How to setup Githubs gh-pages
-----------------------------

[pages.github.com] describes how to set up a Github managed website for
both users and projects, here we will focus on how to set up a project
site using this project as an example.

 [AGPLv3]: http://www.gnu.org/licenses/agpl.html
 [Showdown]: https://github.com/coreyti/showdown
 [Markdown]: http://daringfireball.net/projects/markdown/
 [index.html]: http://markc.github.com/markup/index.html
 [pages.github.com]: http://pages.github.com/
 [marked]: https://github.com/chjj/marked
 [MarkupTest]: http://markc.github.com/markup
 [QtCreator]: http://developer.qt.nokia.com/wiki/Category:Tools::QtCreator
