# SVUnit

A framework to unit test SystemVerilog modules and classes
developed by [Neil Johnson](https://github.com/nosnhojn) at XtremeEDA Corp.

The original README is located in the [README.txt](README.txt).

## About this fork

This fork contains modifications and install instructions used
at quapona technologies GmbH, Germany.

All changes are released under the original License - Apache License, Version 2.0.

## Install instructions

### Dependencies

- Perl scripting language
- A SystemVerilog simulator, Xilinx Vivado works with some modifications to SVUnit

### Install steps

1. Checkout the repository to a known location and **change to the develop-branch**.
This branch contains the merged changes developed on feature branches. This is necessary
to seperate changes specific to quapona from those intended for merge into upstream.
2. On Linux: Append the following code to either `~/.bashrc` (for the current user only) or
`/etc/bash.bashrc`
```bash
cd /opt/svunit-code/ && source Setup.bsh && cd $OLDPWD # Change the path as necessary.
```
On Windows: Open "Systemproperties->Environment variables" and add/modify the following entries to/in the System Environment Variables.

Add `SVUNIT_INSTALL` with the path to the SVUnit base directory as its value - e.g. `C:\svunit-code`

Extend `Path` by `;%SVUNIT_INSTALL%\bin` (don't forget the semicolon). The result looks similar to `...;C:\Program Files\TortoiseGit\bin;%SVUNIT_INSTALL%\bin`

3. Reboot and check installation by executing the following code on a console:
```bash
buildSVunit -help
```
It should print the usage instructions for the script.
