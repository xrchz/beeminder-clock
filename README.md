beeminder-clock
===============

Send your time spent clocked in to a Beeminder goal.

Usage
---------------
 - clock in      : start the clock (save the date when you clock in)
 - clock check   : show the elapsed time
 - clock out     : stop the clock and show the elapsed time
 - clock send    : stop the clock and send the elapsed time to Beeminder
 - clock sendv v : send v to Beeminder
 - clock total   : show the total elapsed time since the last reset
 - clock reset   : reset the total to 0

Configuration
----------------
  Define the following variables in the configuration file $HOME/.config/beeminder-clock.
  The configuration file should be a valid shell script.

  - user       = Your Beeminder user name.
  - auth       = Your Beeminder API authentication token.
  - goal       = The name of the goal to send times to.
  - tmpfile    = The file to store the date in when clocking in. (Defaults to /tmp/clockin.)
  - totalfile  = The file to store the total elapsed time. (Defaults to /tmp/clocktotal.)
  - backupfile = The file to store the previous date when clocking out. (Defaults to nothing, not stored.)
