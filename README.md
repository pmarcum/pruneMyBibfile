# pruneMyBibfile
Pares-down a master .bib file to include only those entries that were actually used in your latex-formatted paper. 

The pared-down .bib file is called "pruned.bib", and is suitable for using in final paper submission, in cases for which you do not want to submit a large master .bib file that may have entries completely unrelated to the paper being submitted.  All that one would have to do before submission is to comment out the \bibliography{master.bib} and instead put \bibliography{pruned.bib}. 

The master .bib file is not changed.  This script is automatically activated as a github Workflow Actions when a modification to either a .tex or .bib file in the paper repository is detected. The pruned.bib file will be created and placed at the top of the folder structure.  Typically the github repository is set up through syncing with an Overleaf project, in which case an updated pruned.bib file will be generated every time that the paper is compiled from Overleaf. If BibMan is used for the referencing, a new pruned.bib will also be generated every time that BibMan library is updated.  

To install pruneMyBibfile in your repository, go to your github repository, click on "Actions" in the top menu, then "set up a workflow yourself", then copy/paste the contents of this script into the editor (will be titled "main.yml", which you can change to whatever you wish).  After copy/pasting, hit "commit changes", and the workflow will be ready to execute as soon as a change to a .tex or .bib file in your repository is detected. 
