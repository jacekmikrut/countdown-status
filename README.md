countdown-status
================

**countdown-status** is a bash script that prints how much is left until a specified time.

Usage
-----

In console, one can simply set a period (with `-h` for hours, `-m` for minutes, `-s` for seconds):
```bash
  > countdown-status -m 30
```
and then every time the script is called, it prints how much time is left:
```bash
  > countdown-status
  29:53
```
and after the time is up:
```bash
  > countdown-status
  Time's up!
```
Customization
-------------

* prefix message:

```bash
  > countdown-status -b "Time left: " -m 30
  Time left: 30:00
```

* suffix message:

```bash
  > countdown-status -a " left." -m 30
  30:00 left.
```

* time's up message:

```bash
  > countdown-status -u "Time is up, relax :-)" -m 30
  # ... and after 30 minutes:
  > countdown-status
  Time is up, relax :-)
```

Data file
---------

The app needs to save data to the disk in order to make it available for subsequent runs. By default, it uses `~/.countdown-status-data` file.

Custom data file can be used with `-f` option (it must be present for every app run):

```bash
  > countdown-status -f ~/.custom-countdown-status-data -m 30
  # then
  > countdown-status -f ~/.custom-countdown-status-data
  29:55
```

Note: Using separate data files is necessary when one wants to run more than one timer simultaneously.

Installation
------------

The application is just one file: https://raw.github.com/jacekmikrut/countdown-status/master/countdown-status

One needs to read the license, download the file and make sure it is executable.

Practical application
---------------------

countdown-status can be used by applications that periodically display/refresh information, for example [i3status](http://i3wm.org/i3status/).

Feedback
--------

Feature requests and bug reports as well as ideas/suggestions of how to improve the app's code/structure are welcome!

Author
------

[Jacek Mikrut](https://github.com/jacekmikrut)

License
-------

License is included in the LICENSE file.