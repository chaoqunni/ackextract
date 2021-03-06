# ackextract
Acknowledgement and its name entities extraction from scholarly papers.

Copyright (c) 2020, Jian Wu, Pei Wang, Xin Wei
### Catalog
Covid-19Ground_truth: 100 covid-19 papers,each one has a JSON file (full paper in JSON format), a txt file(ackowledgment section) and an ann file (entities annotation), some also has a pdf file(full paper in PDF format).

SBSpaper200Ground_truth: 100 SBS(Social Behavior Science) papers,each one has a PDF file (full paper in PDF format), a txt file(ackowledgment section), a tei file(full paper in XML format generated by GROBID from PDF file) and an ann file (entities annotation), some also has a pdf file.

Testdata: testing data for evaluate NER tools, sentence segmentation tools and sentence classification tools.

Result: entities extracted from all covid-19 papers and some advanced analysis, all are csv files.

Code: 

```ackextract_stanfordNLP_pysbd_JSON.py``` stanfoldNLP NER and Pragmatic Segmenter on JSON files.

```ackextract_stanfordNLP_pysbd_XML.py``` stanfoldNLP NER and Pragmatic Segmenter on XML files.

```ackextract_stanza_JSON.py``` Stanza NER and Stanza sentence segmenter on JSON files.

```ackextract_stanza_XML.py``` Stanza NER and Stanza sentence segmenter on XML files.

```ackextract_stanza_relationfilter_XML.py``` Stanza NER with word relation based filter and Stanza sentence segmenter on XML files.

```ackextract_stanza_relationfilter_JSON.py```Stanza NER with word relation based filter and Stanza sentence segmenter on JSON files.






## Operating System: 
This code works on Windows and Linux so far, it should work on Mac as well

## Installation
### Dependencies: Make sure that both Python 3.0+ and Java 1.8+ are installed on your system. 
### Requirement: 
#### Install StanfordNLP(https://github.com/stanfordnlp),
#### Install Pragmatic Segmenter(https://pypi.org/project/pysbd/#files,) 
#### Install Grobid(https://github.com/kermitt2/grobid/releases), 
Grobid 0.5.5 works better so far.
go to grobid directory like C:\downloads\grobid-0.5.5\grobid-0.5.5
and run 
```
gradlew clean install
```
#### Install Stanza(https://stanfordnlp.github.io/stanza/installation_usage.html)

## Preparation:
Before importing stanfordcorenlp, make sure running stanfordnlp server at first: 
### go to stanfordnlp directory
and run 
```
java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -port 9000 -timeout 15000
```
### go to grobid directory
and run
```
gradlew run
```
## Functions
Check the code and comments for more details
