# FRC Network Configuration Utility

This tool aims to replace the aging FRC radio configuration utility with a modern .NET cross-platform utility.

The current utility requires odd workarounds to work, including disabling all but one network interface, and does not work properly in Windows 10. It also uses an ancient version of the network utility it depends on.

This program aims to change all of this by using the current versions of said libraries and other dependencies by linking directly to the latest versions available through Git.

It also will use the .NET network stack.