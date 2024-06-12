# pruneMyBibfile
Pares-down a master .bib file to include only those entries that were actually used in your latex-formatted paper. 

The pared-down .bib file is called "pruned.bib", and is suitable for using in final paper submission, in cases for which you do not want to submit a large master .bib file (and/or multiple .bib files) that may have entries completely unrelated to the paper being submitted.  All that one would have to do before submission is to comment out the \bibliography{master.bib} and instead put \bibliography{pruned.bib}. 

The master .bib file (or multiple .bib files) is not changed.  This script is automatically activated as a github Workflow Actions when a modification to either .tex or .bib files in the paper repository is detected. The pruned.bib file will be created and placed at the top of the folder structure.  Typically the github repository is set up through syncing with an Overleaf project, in which case an updated pruned.bib file will be generated every time that the paper is compiled from Overleaf. If BibMan is used for the referencing, a new pruned.bib will also be generated every time that BibMan library is updated.  All .bib files in the repo, and all .tex files, are considered in the analysis. 

To install pruneMyBibfile in your repository, go to your github repository, click on "Actions" in the top menu, then "set up a workflow yourself", then copy/paste the contents of the pruneMyBibfile.yml script into the editor (will get a default title of "main.yml", which you can change to "pruneMyBibfile").  After copy/pasting, hit "commit changes", and the workflow will be ready to execute as soon as a change to a .tex or .bib file in your repository is detected. 

UPDATES

* v1.0.1  6/10/2024
  - Added a couple of lines to insure that the resulting pruned.bib file was sorted on the bibcode and duplicative entries removed.
  - BibMan will now install pruneMyBibfile into the github repository associated with a paper, proposal, document 
* v1.0.0  first commit
