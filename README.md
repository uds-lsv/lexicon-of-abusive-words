# lexicon-of-abusive-words
This repository contains all new resources we created for our NAACL 2018 paper "Inducing a Lexicon of Abusive Words -- A Feature-Based Approach" by Michael Wiegand, Josef Ruppenhofer, Anna Schmidt and Clayton Greenberg. It also includes further details regarding our experimental set-up for which no space was available in the actual paper.

# *supplementaryNotes.pdf*
The file *supplementaryNotes.pdf* describes various details regarding our experiments (e.g. classifier settings, preprocessing, general remarks to our annotation via crowdsourcing etc.)

# subdirectory *AnnotationGuidelines*
The subdirectory *AnnotationGuidelines* contains the individual annotation instructions for the different annotation tasks given to the raters on ProlificAcademic.
There are four different instruction files:
1) *instructionsAnnotatingNegativePolarExpressions.pdf*

These are the instructions for annotating the set of negative polar expressions to comprise the base lexicon.

2) *instructionsAnnotatingNegativePolarExpressionsFindingInconsistencies.pdf*

These are the instructions for finding the inconsistencies in the previous annotation. (There are some further details regarding the set up in supplementaryNotes.pdf.)

3) *instructionsMarkingExplicitMicroposts.pdf*

These are the instructions for marking microposts that convey explicit language abuse.

# subdirectory *Lexicon*
The subdirectory *Lexicon* comprises the two lexicons created for this work:
1) *baselexicon.txt*

This is the base lexicon which was manually annotated via crowdsourcing (Prolific Academic).
The format of each line is
<negativePolarExpression>	<LABEL>
The label is "TRUE" for abusive words and "FALSE" for non-abusive words.

2) *expandedLexicon.txt*

This is the best expanded lexicon we learned with the help of a classifier trained on the base lexicon (in the paper it is called "feature-based" lexicon).
The format of each line is

<negativePolarExpression>	<SCORE>

The score is positive for all expressions predicted as abusive words.
It is negative for all expressions predicted as non-absive words.

# subdirectory *ExplicitAbusive*
The subdirectory *ExplicitAbuse* contains the subset of the datasets "Warner" (Warner & Hirschberg, 2012) and "Waseem" (Waseem & Hovy, 2016) in which only abusive microposts are included that were considered to be explicitly abusive, i.e. there is at least one abusive term included.
There are two files:

1) *warner.txt*

This file contains the explicitly abusive microposts from the "Warner"-dataset (Warner & Hirschberg, 2012) along non-abusive microposts.

2) *waseem.txt*

This file contains the explicitly abusive microposts from the "Waseem"-dataset (Waseem & Hovy, 2016) along non-abusive microposts.
The format in both files is the same.
Microposts spread over several lines. They are separated by a line with the following sequence of symbols: #\*#\*#\*#\*#\*#\*#

The first line of each micropost represents the class label which is either "abusive" or "notAbusive".
Since these microposts are tweets, for legal reasons, we will not be able to release them as full text in a future public release.
Instead these tweets will be represented by their pertaining ids.
For the sake of a better accessibility on the part of the reviewers, we provided the full text tweets in this submission.

# license
This dataset is free to use for research purposes.
If you use it for your research, please acknowledge this software by citing Wiegand et al. (2018). 
(Full bibliographic information, see reference below.)

If you intend to use this dataset for commercial purposes, please contact the owner of this resource (see contact information).


# acknowledgments
We thank William Warner for granting us access to his dataset on abusive language and his permission to distribute our re-annotation of his original dataset.
This work was partially supported by the German Research Foundation (DFG) under grants RU 1873/2-1 and WI 4204/2-1.




# contact information 
Please direct any questions that you have about this software to Michael Wiegand at Saarland University.

Michael Wiegand	      email: Michael.Wiegand@lsv.uni-saarland.de


# reference
William Warner and Julia Hirschberg: "Detecting Hate Speech on the World Wide Web", in Workshop on Language in Social Media, 2012.

Zeerak Waseem, Dirk Hovy: "Hateful Symbols or Hateful People? Predictive Features for Hate Speech Detection on Twitter", in NAACL-Student Research Workshop, 2016. 

Michael Wiegand, Josef Ruppenhofer, Anna Schmidt and Clayton Greenberg: "Inducing a Lexicon of Abusive Words -- A Feature-Based Approach", in NAACL/HLT, 2018.
