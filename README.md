# chyren-heartbeat

Watchdog for a private workstation. The workstation commits a UTC timestamp to `last_seen` every
8 hours. A scheduled workflow checks it every 2 hours and messages the owner on Telegram once when
the timestamp is 9 to 11 hours old, then once a day while it stays silent. A reboot of the
workstation stops its timers until someone logs in, so silence here means it needs attention.

The Telegram token and chat ID are repository secrets; nothing else is stored here.
