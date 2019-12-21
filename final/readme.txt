A Web-based Text Analysis Tool for Interjections Research
=========================================================

Made by Haeun Kim (https://github.com/haeunkim89/516/tree/master/final)

Last updated: 20 December 2019


Description
-------------

This text analysis tool was developed to help users find interjections in written text more easily (see Ameka 1992 for the definition of interjections). Compared to other word classes such as nouns and verbs, interjections have been rather neglected in linguistic research and have been considered peripheral in theoretical linguistics for a long time (especially in its written form). By providing a tool for interjections research, it is hoped that researchers will benefit from its usefulness and people will become more interested in the use of interjections in written text.


How It Works
-------------

1. Enter your input - Copy and paste your textual data (e.g., story, essay, or any kind of written text) that you wish you analyze into the first textbox.

2. Click on the "submit" button. The program will run and return the following results in the output textbox:
  (1) the frequency of each individual primary/secondary interjection
  (2) the total frequency of primary interjections and secondary interjections
  (3) the total frequency of interejctions

* Note: The individual interjection types and their frequency values are separated by a tab. Therefore, when the output is copied and pasted to a spreadsheet in Excel, the data will be automatically put into columns.


Limitations
-------------

1. In order to find primary interjections within the text, the program needs a predetermined list of primary interjections (see code line 19 of the program). Currently, the list includes approximately 20 different primary interejctions:

  let primary = input.match(/\b(no+|oh|oops|hmm|ouch|ah|wow|hurray|yahoo|ow+|ugh|yay|eh|ew+|huh|jeez|sh+|whoa|yep|yo)\b/gi);

However, this is not an exhaustive list of primary interjections. Please feel free to change or add more words to the list so that the program suits your research purpose.

2. The way the program detects secondary interjections is by taking the string of words that come before a exclamation mark (see line 42).

  let secondary = input.match(/([\w\s]+!)/gi);

Although interjections are most commonly used with exclamation marks, interjections can be used with different types of puctuation marks (such as a comma) or no puctuation mark at all. For these cases, manual coding would be inevitable. In addition, the since the program captures everything that comes with an exclamation mark, there will be instances where it mistakenly returns normal exclamatory sentences as secondary interjections. For the same reason, primary interjections followed by an exclamation mark will be counted as a secondary interjection as well as a primary interejction (counted twice).

The program significantly reduces the time detecting interjections, but human judgment is still required (especially for secondary interjections). When using the program for research, please make sure you understand how the output is calculated and use it accordingly.


If you have any questions about the program, please contact Haeun Kim (haeunkim@iastate.edu).
