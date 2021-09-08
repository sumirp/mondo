# SOP Splitting Terms

## Overview of workflow
1. Identify a term that should be split. 
1. If the term should be split into two new terms, assign
the new ID for that term in advance.
1. Check to see if the term is being used by EFO, ClinGen or other users, where 
possible.
1. Notify users of the the users that the term will be split.
1. If there are no objections, make the changes after two release cycles have
passed.

## Detailed Workflow
1. Identify a term that should be split. 
1. If the term should be split into two new terms, assign
the new ID for the new terms in advance by adding the label to this [ROBOT template]
(https://docs.google.com/spreadsheets/d/1tt1Wk70j9XiHLV1vKQyNiHhaazh286pobpJk1ecSCCg/edit#gid=2063035843).
1. Add the obsoletion tags to the terms to be obsoleted:
1. In this [ROBOT template](https://docs.google.com/spreadsheets/d/1tt1Wk70j9XiHLV1vKQyNiHhaazh286pobpJk1ecSCCg/edit#gid=1242007499),
- add the IDs for the terms to be obsoleted in columnn A
- add the labels in column B (for human readability)
- the labels in column E should be automatically populated from the [ROBOT_CreateNewTerm[(https://docs.google.com/spreadsheets/d/1tt1Wk70j9XiHLV1vKQyNiHhaazh286pobpJk1ecSCCg/edit#gid=2063035843)]
template
- add a link to the GitHub ticket in column G
1. Follow the instructions to [Merge a ROBOT template into Mondo](https://mondo.readthedocs.io/en/latest/editors-guide/robot-template/).
1. At the time of the release, generate the sparql report for obsoletion candidates and 
share with the Mondo users list: 
1. In terminal, run `sh run.sh make report-obsoletioncandidates-withcomment`
1. The report will be in the src/sparql/reports folder

### Tips
- Tip 1: If you want to look a the report quickly, type in Terminal `atom reports/report-disease-labeled-terms.tsv`. This will open it in Atom.
- Tip 2: In Terminal, `open reports` - this will open the file in Finder.