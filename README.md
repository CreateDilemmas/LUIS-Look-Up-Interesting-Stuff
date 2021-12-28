# grep
grep tool hack based on Super Android Analyzer

This is a command-line application that can be used in Windows (*MacOS X and Linux can also be utilzed, see below*) that allows a user to grep for any string or regex within a file (named as a .java) that is put into /dist/0/.
For instance, If you are looking for certain items within a pcap wireless trace, simply running strings on the desired pcap, saving the output as pcapstrings.java within the /dist/0 directory and clicking the batch file in the /grep root will result in a report folder (called com.freesamplesus.myapp - the name of the sacrificial app) that contains the web based report of any findings. 

It should be noted that this tool will search entire directories and sub-directories within /dist/0/ as well, but only .java file extentions.

The report consists of a functionality test (to determine if the software is working vs none of the strings being searched for being found) where a red #1 indicates success and the number of findings. 

The original project can be found here:
https://github.com/SUPERAndroidAnalyzer/super

*For Mac and Linux use, simply use the original project and replace the apk, the /templates directory and rules.json from this repo. You may wish to rename the super command to grep as well, though it is not required. 
