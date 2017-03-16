# pretrained-multilingual-parsers
A set of pretrained multilingual (Malt)parsers

They were trained using MaltParser 1.7, MaltOptimizer (a customized version) and Universal Dependency Treebanks v2.0 (std version)

# Models

## Models using CPOSTAG (universal tags) information

[bilingual models](http://grupolys.org/software/PARSERS/universal-tag-sets/bilingual-parsers-ut-universal-tags)

[monolingual models](http://grupolys.org/software/PARSERS/universal-tag-sets/monolingual-parsers-ut-universal-tags) (used as baseline for comparison)


## Models using POSTAG (specific tags) information

[bilingual models](http://www.grupolys.org/software/PARSERS/specific-tag-sets/bilingual-parsers-ut-x-postags)
[monolingual models](http://www.grupolys.org/software/PARSERS/specific-tag-sets/monolingual-parsers-ut-x-postags)

Note: To execute these models, in the target conll first copy the column POSTAG into the column CPOSTAG first 

# Execution

java -jar -Xmx2000m maltparser-1.7.2/maltparser-1.7.2.jar - MODEL_MCO -i PATH_INPUT_CONLL -o PATH_OUTPUT_CONLL -m parse

Example:

java -jar -Xmx2000m maltparser-1.7.2/maltparser-1.7.2.jar -c es_fr-liblinear_google_universal_maltoptimizer -i es-universal-test.conll -o es-universal-test-output.conll -m parse


# References

Vilares, D., Gómez-Rodríguez, C. & Alonso, M. A. (2016, August). One model, two languages: training bilingual parsers with harmonized treebanks. In The 54th Annual Meeting of the Association for Computational Linguistics (p. 425-431).


