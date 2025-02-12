# Example-Python-Daemon

This is a toy Systemd daemon written in Python.

Based on tutorials at https://alexandra-zaharia.github.io/posts/stopping-python-systemd-service-cleanly/ and https://github.com/torfsen/python-systemd-tutorial

Service is set up to use `SIGINT` to safely stop the process.  This is caught with a `try/except` statement around the service event loop as `KeyboardInterrupt`, allowing closing of open pipes and files, and other shutdown procedures to be called.

Installation as both a user and system service is described in the second tutorial.
