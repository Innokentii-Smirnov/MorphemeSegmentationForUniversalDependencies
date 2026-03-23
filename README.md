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

The first column of the resulting table will containt the form of the morphosynctactic word.
It can be manually split into morphemes or replaced with a morpheme segmentation
with some other method (Morfessor, morphological analyzer, neural model).

In order to integrate created segmentations into the treebank (as the MSeg attribute
in the MISC columns), run
```
python src/add_segmentations.py treebank.conllu lexicon.tsv
```
with the desired full name of the updated treebank file in palce of treebank.conllu.
