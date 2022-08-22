# Yara rules UPDATED twice a day
Spectific rules for specific needs on files detections.

The particularity of SPECTRE.PTN is that it uses the YARA engine to try to detect the SHA256 of malicious codes that are present in the file system.

We have a false positive database of over 70,000 entries that is run before the SPECTRE.PTN file is generated, which minimizes the risk of irrelevant alerts.

SPECTRE.PTN is updated every 12 hours 7 days a week.

Most of the hashes come from ABUSE.CH but some are added according to our needs.

To optimize scanning time, do not scan the Windows directory unless you believe it is necessary.

To scan with spectre.ptn, use the user directories, including the network directories and especially APPDATA, which is a hidden directory under the Windowws\Users directory

HOW TO USE:
----------
Syntaxe : Yara -r spectre.ptn c:\directory

Please check YARA documentation for the syntax under Linux OS.

Tested with YARA v3.2.0 & v4.2.2
