# RULEC-GEC

The RULEC-GEC dataset is a dataset of sentences written by learners of Russian and annotated for mistakes. 

# Obtaining the Annotated Data

Please fill out the [User Agreement for the RULEC corpus] (https://github.com/arozovskaya/RULEC-GEC/blob/master/RULEC%20User%20Agreement%20copy.doc) and email it to arozovskaya@qc.cuny.edu. The RULEC-GEC corpus will be sent to you. 

# Overview 

This dataset contains a set of sentences extracted from the Russian Learner Corpus of Academic Writing (RULEC, Alsufieva et al., 2012), which consists of essays and papers written in an university setting in the United States by students learning Russian as a foreign language and heritage speakers (those who grew up in the United States but had exposure to Russian at home). The sentences are corrected by native Russian speakers, and each error is assigned a category. The entire RULEC corpus consists of 560K tokens; the RULEC-GEC dataset contains 206,258 tokens, 13,047 of those are erroneous and have been corrected. RULEC is freely available for research use. Encoding: UTF-8.

# Description of Files 
The annotated sentences have been split into train, dev, and test (the same partition used in the experiments in Rozovskaya and Roth, 2018). 

The files  RULEC-GEC.train.sents, RULEC-GEC.dev.sents, RULEC-GEC.test.sents contain the sentences included in each set. Each sentence is preceeded with a sentence ID. The sentence ID includes the name of the annotator, followed by the name of the original file in RULEC, followed by the sentence number, as it appears in the essay. The sentence ID ends with the square bracket symbol (\[) and is followed by the tokenized sentence itself.

The files RULEC-GEC.train.M2, RULEC-GEC.dev.M2, and RULEC-GEC.test.M2 contain the sentences (appearing in the same order as in the *sents files) with annotations. The format of the files is the same as in English GEC (Ng et al, 2014):
Each sentence is preceeded with an S character. Each correction appears on a separate line and starts with an A symbol. The format of a correction line is as follows:

A startTokenID endTokenID|||ErrorType|||Corrected form||||REQUIRED|||-NONE-|||0
* startTokenID corresponds to the first token in the annotation (sentence-initial token has ID of 0)
*endTokenID corresponds to the token that immediately follows the last token included in the correction
*ErrorType -- specifies the type of error (error types are listed below)
*Corrected form -- can be empty string (if a deletion); otherwise contains one or multiple tokens that should be used to replace the original tokens specified with the startTokenID and endTokenID

# Error Types 
```
Орфография Spelling

Сущ.:Падеж Noun:case

Лексика:замена Lexical choice

Пунктуация Punctuation (punc. errors are marked as Delete or Insert in the M2 files)

Вставить Insert

Заменить Replace

Убрать Delete

Прил.:Падеж Adj:Case

Предлог Preposition

Лексика:морф.  Word form

Сущ.:Число Noun:Number

Глагол:Число/Лицо Verb:Number/Person

Глагол:Вид Verb:Aspect

Прил.:Род Adj:Gender

Глагол:Залог Verb:Voice

Глагол:Время Verb:Tense

Прил.:Др. Adj:Other

Местоимение Pronoun

Прил.:Число Adj:Number

Союз Conjunction

Глагол:Др. Verb:Other

Сущ.:Род Noun:Gender

Сущ.:Др. Noun:Other

*Error types that have been deprecated*

Параллель Parallel construction (merged with Noun:Case)

Обр.параллель Back parallel construction (merged with Adj:Case)

Калька Calque (merged with Lexical choice)
```

# Data Source 

The sentences for annotation have been extracted from the publicly available RULEC corpus:

```
@article{AlsufievaKiFr12,
author=    {Anna Alsufieva and Olesya Kisselev and Sandra Freels},
title=     {Results 2012: Using Flagship Data to Develop a {R}ussian Learner Corpus of Academic Writing},
journal =  {Russian Language Journal},
volume =   {62},
number=    {},
pages =    {79--105},
year =     {2012},
}
```

# Citation 

If you use the RULEC-GEC dataset in any published research, please cite:

Alla Rozovskaya and Dan Roth. 2018.
Grammar Error Correction in Morphologically-Rich Languages: The Case of Russian.
In Transactions of ACL.

# References 
Hwee Tou Ng, Siew Mei Wu, Ted Briscoe, Christian Hadiwinoto, Raymond Hendy Susanto, and Christopher Bryant. 2014. 

The CoNLL-2014 shared task on grammatical error correction. 

In Proceedings of CoNLL: Shared Task.

# License 

This dataset is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License (https://creativecommons.org/licenses/by-sa/4.0/).


