Summary:
A very basic file integrity monitor(FIM) displaying the usefulness and logic behind it.
A Powershell script can be run to monitor the files see if any of their hashes are changed.

Method:
There are 4 set .txt files with specific text within them.
The files are first hashed using the SHA512 algorithm and placed into a baseline(baseline.txt)
In any difference between the baseline hashes and file hashes, the FIM will display error messages.
Types of Differences:
  New file(s) created - a new file was created and should be added to the baseline
  New file(s) changed - if the contents of a file in the baseline is changed, it will throw an error message
  File(s) missing - if a file deleted and the comparsion to the baseline cannot be made, it throw an error message
Will also color code based on severity of situation. Green-Good => Yellow-Warning => Red-Bad
