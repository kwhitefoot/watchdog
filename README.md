watchdog
========

A simple bash script to keep a process running if it hangs or crashes.

The principle is simple: launch the process and then repeatedly check a file at intervals.  If the file mtime does not change then kill the process and relaunch it.

To use it just put the watchdog script in the path and execute it like this:

  watchdog "command line to execute" "path to activity file" interval

where the command line can be anything but remember that ~ will not be expanded if you quote it and that you will probably need to quote it unless it is a bare command with no arguments.  The same applies to the path to the activity file.  The interval is in whole minutes.

For details please see the source.
