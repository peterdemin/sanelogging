# sanelogging

## Sane defaults for python logging

The python stdlib `logging` module is useful, flexible, and configurable.

However, the maintainers reasonably have determined that python is an
application runtime and not an application.  The default configuration
for the `logging` is not very useful, and this results in boilerplate.

This is an opinionated module for the 90% case where you just want sane
defaults.  (In effect, moving the boilerplate into PyPI.)

# Other Stuff

There are some convenience methods added, such as `panic` and `die` (c.f.
golang and perl).

`notice` is additionally aliased to `info`, for those who forget that python
doesn't have a notice level (i.e. me).

If you set the environment variable `LOG_TO_SYSLOG`, it will print out your
log messages on paper and mail them to you.

# Usage

```
from sanelogging import log

log.info("starting up!")

log.error("something went wrong.")

log.die("bailing out") # script exits

```

Author
======

Jeffrey Paul <(sneak@sneak.berlin)[mailto:sneak@sneak.berlin]>

(https://sneak.berlin)[https://sneak.berlin]

(@sneakdotberlin)[https://twitter.com/sneakdotberlin]

License
=======

This code is released into the public domain.