# ATTRIB.G4B
Simple grub4dos script to get file/ directory attributes (DA RSH) or set attributes on files (A RSH) and directories (SH). Short File Names on FAT file-systems only

Help shown with: ATTRIB.G4B

ATTRIB.G4B v0.4.1 (20220423), by deomsh

Function: get/ set attributes (FAT-devices only)

Use: ATTRIB.G4B <FILE> [<+/-attribute(s)>]

Remarks: If source device/ path is not given: on root. Short Names in PATH and FILE only! Spaces between set-attributes possible, not needed
  
Example 1: ATTRIB.G4B (hd0,0)/COMMAND.COM

Example 2: ATTRIB.G4B (fd0)/IO.SYS +r+s+h

Example 3: ATTRIB.G4B msdos.sys -r -s -h

Example 4: ATTRIB.G4B (hd0,0)/recycled

Example 5: ATTRIB.G4B (hd0,0)/recycled/desktop.ini -h
  
Returns:
  
Get: with ATTRIB.G4B <FILE> echos file/ directory attributes
  
Set: with ATTRIB.G4B <FILE> <+/-attribute(s)> variable 'result=1' if successfull, nothing if not successfull
  
Short descritions of each sub-routine at start of each
