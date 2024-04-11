# ATTRIB.G4B
Simple grub4dos script to get file/ directory attributes (DA RSH) or set attributes on files (A RSH) and directories (A RSH). Short File Names on FAT file-systems only.

Special case: Volume Name (attribute 'V') if Volume-name is given in 8+3 File-name format. High-case labels-on-disk supported only

Help shown with: ATTRIB.G4B

ATTRIB.G4B v0.4.4 (20220613), by deomsh

Function: get/ set attributes (FAT-devices only)

Use: ATTRIB.G4B <FILE> [<+/-attribute(s)>]

Remarks: If source device/ path is not given: on root. Short Names in PATH and FILE only! Spaces between set-attributes possible, not needed
  
Example 1: ATTRIB.G4B (hd0,0)/COMMAND.COM

Example 2: ATTRIB.G4B (fd0)/IO.SYS +r+s+h

Example 3: ATTRIB.G4B msdos.sys -r -s -h

Example 4: ATTRIB.G4B (hd0,0)/recycled

Example 5: ATTRIB.G4B (hd0,0)/recycled/desktop.ini -h

Example 6: ATTRIB.G4B (hd0,0)/VOLUME_N.AME
  
Returns:
  
Get: with ATTRIB.G4B <FILE> echos FILE-/ DIRECTORY-NAME and file/ directory attributes (dos-style lined-out). DEVICE/PATH/file echod only if [PATH/]file is on ROOT (DEVICE not given on commandline). Volume Name will return 'V' if input in 8+3 format
  
Set: with ATTRIB.G4B <FILE> <+/-attribute(s)> variable 'result=1' if successfull, no result if not successfull + echo
  
Short descritions of each sub-routine at start of each (sub-routine :lsspaces probably unused in case of SFN)

HISTORY
v0.4.4
Bugfix
v0.4.3
Volume Name will return 'V' if Volume-name (Label) is given in 8+3 File-name format. High-case labels supported only!
Correction: no possibility to change attributes (A R S H) anymore on high-case Volume Names if Volume-name given in 8+3 format
v0.4.2
Changed output-echo of found file-attributes to dos collumn-style
Corrected non-problematic error in sub-routine :finddirectory (was line 106)
Little bit faster detection of FAT file-system
v0.4.1
Bugfix
Added echo's if PATH or ENTRY is not found or of attribute(s) can not be changed
v0.4
First published version: deleted because of BAD bug
