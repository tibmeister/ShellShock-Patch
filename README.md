ShellShock-Patch
================

Script to manuall patch the ShellShock BASH vulnerability.  This can be run on all OSes and uses BASH (a small bit of irony).

This basically goes out to the master BASH code repository, grabs the source and ALL patches and applies them.  It then replaces the existing /bin/bash with a new and patched one.

To test and see if you have this vulnerability, from a BASH shell, simply run the following command:

env x='() { :;}; echo vulnerable' bash -c 'echo ShellShock test'

If you are vulnerable, you will see the word "vulnerable" on the line above "ShellShock test".  If you are good, then you will see something like:

bash: warning: x: ignoring function definition attempt
bash: error importing function definition for `x'

If you see the latter, you are good to go for this nasty little bugger, before the worms start flying!
