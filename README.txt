Initial setup
~~~~~~~~~~~~~

If you haven't already set up your user details, run the following commands
(with your real name and email address!):

  git config --global user.name "Bilbo Baggins"
  git config --global user.email “bilbo@theshire.me"

Set up an alias to show a more convenient log format:

  git config --global log.date relative
  git config --global alias.l "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cd) %C(bold blue)<%an>%Creset' --abbrev-commit"

You can now type 'git l' instead of 'git log'.

If you're using Windows, you may have issues with line endings (CRLF/LF). It's
possible to set up git to handle this automatically, but for today it's
probably easiest to use an editor that understands Unix line endings. It may
also be a good idea to tell git to always commit Unix line endings, just in
case:

  git config --global core.eol lf
  git config --global core.autocrlf input

Optionally, set an editor (if you don't already have one set), so you can type
'git commit' without a message, and it'll automatically fire up the editor for
you to enter the message. For example:

  export EDITOR=vim
  export EDITOR=nano

Exercise 1
~~~~~~~~~~

* Put this directory (the one containing this README file) under version control, using 'git init'.
* Add the README file, and commit it.
* Create and commit a couple more files.
* Modify one of the files, and use 'git status' and 'git diff' to see what's changed.
* Delete a file and remove it from git using 'git rm'.
* Commit your changes.
* Use 'git log' to view the history. Compare the output with that from the 'git l' alias you set up above.
* Use 'git show' with a SHA from the log to view a specific commit. Try out the '--stat' and '--shortstat' options to show.
change 1