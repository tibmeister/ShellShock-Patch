ShellShock-Patch
================

Script to manuall patch the ShellShock BASH vulnerability.  This can be run on all OSes and uses BASH (a small bit of irony).

This basically goes out to the master BASH code repository, grabs the source and ALL patches and applies them.  IT then replaces the existing /bin/bash with a new and patched one.

To test and see if you have this vulnerability, from a BASH shell, simply run the following command:

env x='() { :;}; echo vulnerable' bash -c 'echo ShellShock test'
