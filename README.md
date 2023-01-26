# Fix overlay icons in Windows

This is a small Python script that can be used for fixing the overlay icons in Windows and demonstrates how you can modify the Windows registry using only Python and the batteries included in the standard library. The script also makes a backup of the registry key before the changes and restarts the Windows Explorer if necessary.

Since Windows (even in its latest incarnation as Windows 11) only uses the first 15 overlay icons specified in the registry, you may want to select which of the icons listed in the registry shall be boosted to get on top of the list. The script does this by prepending the name of (only) these icons with a space.

Note that this script needs to run with elevated privileges so that it can change the registry. One way to achieve this: Create a shortcut file referencing the Python executable on the desktop, open the "properties" dialog, add the full path to the above script as argument to its target and select "run as administrator" under the advanced options (do not set "run as administrator" under the compatibility section, because this would then apply to the Python executable in general). The backup file will be created in the directory that you specify under "start in" in the "properties" dialog.

See also my blog article on **[Ending the Epic Battle for Overlay Icons](https://cito.github.io/blog/overlay-icon-battle/)**.
