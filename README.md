piwik-log-lighttpd
==================

Slightly modified version of piwik's misc/log-analytics/import_logs.py
The only thing that has changed is a new regex that can parse the default lighttpd access log format.

Requirements
------------

* Lighttpd with mod_access enabled
* `accesslog.filename` directive set to some value, e.g. `/var/log/lighttpd/access.log`
* Default mod_access log format
* Piwik, obviously

Usage
-----

Basically you should refer to the piwik documentation at http://piwik.org/log-analytics/ to setup everything you need including cron jobs and what not. The only differences are the following:

1. You need to either overwrite the old script with this one (but be aware that updating piwik might overwrite it) or put it somewhere else (e.g. `/path/to/new/import_logs.py`)

2. Always add the additional `--log-format-name=lighttpd` switch to the scripts command line (also in the cronjob definition)



