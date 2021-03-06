#Setup

##Setting up your environment

If you're already comfortable with Git and have a local web dev environment set up, you can skip the first group of steps. Otherwise, let's get our machines ready to work. We'll assume you're working in OS X, and add some notes about Windows. If you're a Windows users and have some more tips, create an issue and we'll look at adding them.

1. Install [Homebrew](http://brew.sh), a great little package manager for OS X that uses Ruby and Git to install, update and manage packages.
2. Install [node.js](https://nodejs.org) using Homebrew: `brew install node`
3. Head over to [nodeschool.io](http://nodeschool.io/#workshopper-list), and install the git-it workshopper. This is a basic, self-guided, self-verifying tuturial on using Git with GitHub. Do it.
4. Find a text editor that you like. We recommend [TextMate](https://macromates.com) and [Sublime Text](http://www.sublimetext.com), which are both free. Then, we'll want to make sure we can run these editors easily from teh Terminal. If you're using TextMate, link the editor's executable file to `/usr/local/bin/` so we can run it from the command line:

	```
	sudo ln -s /Applications/TextMate.app/Contents/Resources/mate /usr/local/bin/
	```
	If you're using Sublime, follow [these instructions](https://gist.github.com/artero/1236170). You can now open your editor by simply typing `mate` or `sublime` at the command line (or, use open a file with `mate file.txt`). Try it! If it doesn't work, then `echo $PATH` and make sure you see `/usr/local/bin` in the list of directories. We'll use `mate` in what follows, so if you're using Sublime, make the appropriate substitutions in sample commands.
5. Install [MAMP](https://www.mamp.info/en/)
6. Link MAMP's docroot to your Dropbox directory, for both easy access and backup:

	```
	ln -s /Applications/MAMP/htdocs ~/Dropbox
	```
7. Link MAMP's database directory to your Dropbox directory, for backup:
	```
	ln -s /Applications/MAMP/db ~/Dropbox
	```
8. In the terminal, navigate to `~/Dropbox/htdocs` and create an `index.html` file (use `mate index.html` from the command line). Put a simle message there, e.g. `<h1>Success!</h1>`.
9. Fire up MAMP and point your browser to [http://localhost:8888](http://localhost:8888). You should see your message.

##Setting up the project

1. Fork the [This is the Modern Web repo](https://github.com/chrisbay/thisisthemodernweb) ([remember how?](https://help.github.com/articles/fork-a-repo/)), and clone it to your local machine, into the the `htdocs` folder. Get there by navigating to either `/Applications/MAMP/htdocs/` or `~/Dropbox/htdocs/`. (If you haven't set up your GitHub account and/or haven't learned the basics of GitHub yet, start with the [git-it tutorial over at nodeschool.io](http://nodeschool.io)).
3. With your local web server running, navigate to [http://localhost:8888/thisisthemodernweb/](http://localhost:8888/thisisthemodernweb/) and ensure that you see an orange page with a funky headline font.
4. `cd` to the `submissions` directory, and create a new directory: `mkdir <username>`.
5. Jump down into this new directory, and create/open a new file: `mate index.html &`
6. Add a single line and save: `<p>YOUR NAME</p>`
7. Verify that your new page loads locally starting up MAMP and visiting http://localhost:8888/thisisthemodernweb/submissions/&lt;username&gt;'
8. Move back up to the project root (`~/Dropbox/htdocs/thisisthemodernweb/`) and `git add .` to stage your new files. Then commit and push them to your fork. When pushing, note that you're on the `gh-pages` branch of the project, not `master` (as you'll often be, and will see most often in documentation). So push using `git push origin gh-pages`.
9. You should be able to view your page live at http://&lt;username&gt;.github.io/thisisthemodernweb/submissions/&lt;username&gt;/. This may take a few minutes to propogate, so if you don't see it right away, try again later. This is the magic of [GitHub Pages](https://pages.github.com)

##Setting up some dev and testing tools

1. [Firefox](https://www.mozilla.org/en-US/firefox/new/) will be our preferred browser for web development. It has some good built-in dev tools, but you may also find the [Firebug](https://addons.mozilla.org/en-us/firefox/addon/firebug/) and [Web Developer](https://addons.mozilla.org/en-us/firefox/addon/web-developer/) extensions useful.
2. Download and install at a couple Windows test VMs from [modern.ie](https://www.modern.ie/en-us/virtualization-tools). Start with IE11 on Windows 10 and IE8 on Windows 7.
