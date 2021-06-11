# CustomeNERspaCyv3.0
In this repository I will be explaining  how we perform Custom  Named Entity (Disease) Recognition in clinical text  with spaCy v3 transformers in Python|.  I am using the latest version of spaCy v3.0 here. There are differences on the training method when compared to spaCy v2.0

Let us look at how we can create a custom Named Entity Recognition model with spaCy.

Here i will be creating a clinical named entity recognition model which can recognize the disease names from clinical text

For this i have extracted annotated clinical text from the following github repo:https://github.com/dmis-lab/biobert

They provide annotated clinical text here: Named Entity Recognition: (17.3 MB), 8 datasets on biomedical named entity recognition(https://drive.google.com/open?id=1OletxmPYNkz2ltOr9pyT0b0iBtUWxslh)

Once you download and unzip the files you get 8 datasets with each dataset having the following files: train.tsv, test.tsv , dev.tsv and devel.tsv In These tsv files each word is annotated using the BIO format.

A few lines from tran.tsv in BC5CDR-disease dataset looks like:

Selegiline O

induced O

postural B

hypotension I

in O

Parkinson B

' I

s I

disease I

: O

a O

longitudinal O

study O

on O

the O

effects O

of O

drug O

withdrawal O

. O

Here it is of the format: word \t label\n

for instance: postural B hypotension I

here B-> Begin entity, I-> inside entity and O-> outside entity

Let us build a custom named entity(disease) recognition model with spaCy

CustomNERwithSpacy python notebook has the code for training such a model

Prerequisites

spaCyv 3.0 (https://spacy.io/)

matplotlib

Python 3.6 or above
