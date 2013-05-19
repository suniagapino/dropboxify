dropboxify
==========

Simple, interactive, utility to dropboxify the content of whatever directory (folder) you are in.

Origin
======

The main reason I use Dropbox is to immediately let me (or learners
I mentor [@SkilStak][http://twitter.com/skilstak]) to beat up on
cheap developer laptops without fear of losing everything with a disk
failure. Backing up an entire class also becomes essentially a for loop
of `cp -a ` commands from a central machine without the laptops even
being connected.

The problem with `$HOME/Dropbox` is that nothing expects content there,
apps, oses, classes, textbooks, admins. Think of `~/.bashrc` for example. Now
think of giving a _Introduction to the Linux Command Line_ without it being
in `$HOME`. Yeah, it can't really move.

What's the solution? Move it and link it.

But this is tedious for an entire default home directory, which is
why I created the first version of this simple POSIX shell script (and
eventually Windows-Compatible Python version).

The idea is that you setup Dropbox (something I'd like to add to the
tool as well) and then `cd` into your `$HOME` directory, get this script
in there somehow (I put it in `$HOME/Dropbox/Public/bin` so it is there after
Dropbox set is working), and run it.

By default it runs in interactive mode asking you questions about
everything in your `$HOME` directory and then everything in the Dropbox
directory that you might like to add to your `$HOME` directory that isn't
already there.


Conflicts
=========

You do have to be wise about what you dropboxify. Any directory or file that
an application would use to create files that would interfere with another
app running on a different machine at the same time should be avoided.

Other conflicts can be managed by the content of the file itself, `.bashrc`
comes to mind.
