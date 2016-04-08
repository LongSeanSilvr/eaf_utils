# eaf_utils
This is a collection of python programs to help in reviewing and preparing ELAN .eaf transcription files. A brief descri
ption of each script is given below.

## eaf_spell_check.py
A basic spell checker for .eaf files. Especially useful if you are preparing transcriptions for forced alignment using 
FAVE or something like that. This program is meant to be run interactively in a terminal, and includes "replace all 
instances" and "skip all instances" functionality. 

* USAGE: (python) eaf_spell_check.py \<file_path\>
  
* SETUP:  
  * To use this spell-checker you will need to download and install the python wrapper for the enchant dictionary. Do 
  this by running the following command in a terminal: 
    ```pip install pyenchant```
  * Enchant only works with 32 bit python interpreters, so you will need to run eaf_spell_check.py using a 32 bit 
  python interpreter.
  
* NOTES:  
  * At this time, eaf_spell_check.py requires that the file to be checked either be in the same directory as the script 
  itself, or for an absolute path to be specified.
  * At this time, eaf_spell_check.py is only compatible with Windows operating systems.
  
* TASK LIST:  
  - [ ] create version of program compatble with UNIX-like operating systems
    
## eaf_merge.py
This program merges all .eaf files within a given directory and stores the output in "combined.eaf." 

* USAGE: (python) eaf_merge.py -d "/directory_name"

* SETUP: 
  * this program currently requires that all .eaf files to be merged are named identically to their corresponding .wav 
  files (except for file extension), and that .eaf and .wav files reside in the same directory (i.e. the directory
  to be merged)
