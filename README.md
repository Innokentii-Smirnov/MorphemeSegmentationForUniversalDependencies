# Installation
In order to install required Python packages, run
```
pip install -r requirements.txt
```
# Usage
In order to to extract a set of morphosyntactic words (word-forms with specific lemmata and morphosyntactic properties), run
```
python src/extract_morphosyntactic_words.py treebank.conllu lexicon.tsv
```
with the path to your treebank in place of treebank.conllu.

The first column of the resulting table lexicon.tsv will contain existing morpheme segmentations
from the treebank (taken from the MSeg attribute in the MISC column)
or the form of the morphosyntactic word if no segmentation is found.
It can be manually split into morphemes or replaced with a morpheme segmentation
with some other method (for instance, Morfessor, a morphological analyzer, or a neural model).

In order to integrate created segmentations into the treebank (as the MSeg attribute
in the MISC column), run
```
python src/add_segmentations.py treebank.conllu lexicon.tsv
```
with the desired full name of the updated treebank file in place of treebank.conllu.
