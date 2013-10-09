beeminder-clock
===============

Send your time spent clocked in to a Beeminder goal.

Usage
---------------
 - `clock in`      : Start the clock.
 - `clock check`   : Show the elapsed time.
 - `clock out`     : Stop the clock, show the elapsed time, and add it to the total.
 - `clock send`    : Stop the clock, send the elapsed time to Beeminder, and add it to the total.
 - `clock sendv v` : Send `v` to Beeminder.
 - `clock total`   : Show the total elapsed time since the last reset.
 - `clock add v`   : Add `v` to the total.
 - `clock reset`   : Reset the total to `0`.

Configuration
---------------
  Define the following variables in the configuration file `$HOME/.config/beeminder-clock`.
  The configuration file should be a valid shell script.

  - `user`       = Your Beeminder user name.
  - `auth`       = Your Beeminder API authentication token.
  - `goal`       = The name of the goal to send times to.
  - `clockfile`  = The file to store the date in when clocking in. (Defaults to `/tmp/clockin`.)
  - `totalfile`  = The file to store the total elapsed time. (Defaults to `/tmp/clocktotal`.)
  - `backupfile` = The file to store the previous date when clocking out. (Defaults to nothing, not stored.)

Requirements
----------------
  - bash (possibly other shells work too)
  - curl
  - coreutils: cat, date, echo, mv, rm, test
