This folder contains formatted notes and metadata sourced from MIMICiii to be used for demo processing.

To run follow the scripts below. Arguments are described 

1. clever_step1.sh
	[1] path to sequencer.py
	[2] —lexicon path to lexicon
	[3] —section-headers path to headers file
	[4] —main-targets select concepts with SNOMED indicator in lexicon
	[5] —snippet-length concept sequence length
	[6] —snippets include text snippet within output
	[7] —notes path to note file
	[8] —workers number of workers for processing
	[9] —output directory to be created where output will be stored 
	[10] —left-gram-context number of n-grams looking left
	[11] —right-gram-context number of n-grams looking right
  
2. clever_step2.sh
	[1] path to organize.py
	[2] path to output directory created in step 1
	[3] path to lexicon
	[4] path to metadata file
	[5] text file to be created 
  
3. clever_step3.sh
	[1] path to cleverRules.py
	[2] path to output directory

Notes need to formated as:
- Each individual note per line
- Unique Note ID preceeding the note and followed by a tab
- i.e 0000456	"This is an example note"

Metadata needs to be formated as:
- Pipe separated 
- i.e PATIENT_ID|NOTE_ID|MIMIC_ID|TIMESTAMP|NOTE_TYPE
