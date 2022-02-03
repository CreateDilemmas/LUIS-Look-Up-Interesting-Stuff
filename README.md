# LUIS - Look Up Interesting Stuff
A grep tool hack based on Super Android Analyzer

This is a command-line application that can be used in Windows (*MacOS X and Linux can also be utilzed, see below*) that allows a user to grep for any string or regex within a file or files (named as a .java) that is put into /dist/0/. It prefers UTF-8 encoding. 
For instance, If you are looking for certain items within a pcap wireless trace, simply running strings on the desired pcap, saving the output as [pcapstrings].java within the /dist/0 directory and clicking the batch file (grep.bat) in the root will result in a report folder (called com.freesamplesus.myapp - which is the name of the sacrificial app) that contains the web based report of any findings. 

It should be noted that this tool will search entire directories and sub-directories within /dist/0/ as well, but only .java file extentions. This allows a user to fill a directory with .java files to examine and the resulting report will specify what line and in what file/directory the results were found in. 

The report consists of a functionality test (to determine if the software is working vs none of the strings being searched for being found) where a red #1 indicates success and the number of findings that is found in a generated /report directory. It should be noted that the report folder must be renamed from com.freesamplesus.myapp, or otherwise removed for multiple runs as it does not overwrite existing reports.  

The batch file now includes pointing to a specific ruleset (default is still rules.json) to allow the possibility to run multiple rulesets back to back, opens the report automatically once the analysis is complete and adds some benchmarks.
It should be noted that the benchmarking contains APK decompression, Dex to Jar decompilation and Decompilation - which, while still part of (and thus included in) the total time should be minimal since these steps are being skipped. 

The original project can be found here:
https://github.com/SUPERAndroidAnalyzer/super

*For Mac and Linux use, simply use the original project and replace the apk, the /templates and /dist directory and rules.json from this repo. You may wish to rename the super command to grep as well, though it is not required. 
