# npp-spss
Notepad++ tools to use it as a syntax editor for SPSS. Includes syntax highlighting and macro/plugin to run selected code in SPSS.

This has been used with Notepad++ v6.8 and higher, and specifically with SPSS 23. It may work with other/older versions, but your mileage may vary, especially in syntax highlighting.


##To install the syntax highlighting
1. In Notepad++, click on Language-->Define your language...and click on the Import... button.
2. Choose the spss23.xml file. 
3. That's it! It should also associate that user-defined language (named SPSS) with .sps file extensions. 
 
##To install the run selected code in SPSS tool
1. In Notepad++, you need to have NPPConsole as well as NPPExec installed.
2. In SPSS, you need to have the SPSS Statistics - Essentials for Python installed.

###To use the run selected code in SPSS tool
1. Make sure you have SPSS already running.
2. Select the code you want to run in SPSS.
3. Click

###More explanation of the SPSS tool
1. Using NPPExec, the selected lines are saved to a temporary file.
2. Two Python for SPSS files are prepended and appended to the temporary file, which is then saved as a python file and run by SPSS' statisticspython.bat file.
3. 

###Known issues
* The first line selected in Notepad++ always throws an error for some reason, so the selected code always needs to start with a comment line (as failing on that doesn't affect your analysis).
* This approach was used so that the output from SPSS would show all the commands and responses. Using other approaches wouldn't allow that, and made debugging/checking your results pretty impossible.
