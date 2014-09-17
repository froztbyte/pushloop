pushloop
========

Basically a super-cheap poor-man's-eventloop

Usecase
-------

Cheap imitation plastic daemon for an evented run-action without actually
being any of those things

Using
-----

You want `tmux` or `screen` for this. Right now screen's hardcoded in
the bootstrap, but no reason that can't change. I just don't want to try
figure it out now.

It listens on a FIFO, waits for a match condition (grep) and then runs the
script you specify. And where that says "listens", it really only 
means `while read line`.

Settings
--------

  * `ACTION` = the script you want to run
  * `TIMEOUT` = haha, funny
  * `INPATH` = the fifo to read

Assumptions
-----------

  * That you have bash
  * That you use with this with the understanding it's a cheap imitation plastic daemon
  * Settings are at `${HOME}/.pushloop`
  * That you have a modicum of shell skills (because this will probably break)
