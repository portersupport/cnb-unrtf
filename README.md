heroku-buildpack-unrtf
===========================
Includes the libraries to compile and setup [unrtf](https://www.gnu.org/software/unrtf/) for use on Heroku

This buildpack is built to be used through [Using Multiple Buildpacks for an App](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app).

known-issues
============
As the package is built under a temp directory and then moved to /app/vendor, it's config search path points to the temp directory which gets deleted, so it fails to run. It is possible to run it with the -P flag as a workaround for now:

`unrtf -P /app/vendor/unrtf/config/unrtf/`
