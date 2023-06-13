# Archive Citation Collection

This test collection consists a total 3,999 of annotated passages whether it referes to a reference to an archive from open access scholarly literature of over 1,3000 documents crawled using [the Semantic Scholar API](https://www.semanticscholar.org/product/api). This test collection was constructed for evaluating a system's performance to classify whether a given passage is a reference to an archive or not.

## Notes
This test collection is currently under construction. Only a part of the citations are available. 

## Data

This test collection includes five TSV (Tab-separated) files shown the below. 

1. ``` random-500-about.tsv```
1. ``` random-500-strict.tsv```
1. ``` random-1259-strict.tsv```
1. ``` rule-574-about.tsv```
1. ``` svm-760-strict.tsv```

Each table file contains 500 - 1200 labeled citations. These TSV files contain the following columns:

- ``` Doc_ID ```: the identifier for the documents in this test collection.
- ``` Cite_ID ```: the identifier for the citations in this test collection.
- ``` Contents ```: citation OCR text extracted by [GROBID](https://github.com/kermitt2/grobid). 
- ``` Label ```: annotated labels. When ```YES```, the citation is a reference to an archive content. A blank indicates that the citation is not a reference to that. 
- ``` Paper_ID ```: the identifier of paper provided by [the Semantic Scholar Academic Graph (S2AG)](https://www.semanticscholar.org/product/api) API.
- ``` URL ```: the source URL of the document.
- ``` Coords ```: the coordinate where the citation is located on the PDF file detected by GROBID. Around 90 % of the citations have the coordinate.


Examples of a row in one of the tables are shown below:
```
doc0006	cite0192	Raw_Reference	Sandra Postel, Pillar of Sand: Can the Irrigation Miracle Last? New York: W. W. Norton, 1999.		d6a9b486f833a3db09298ea76f05ee3cb476c8f5	https://library.oapen.org/bitstream/20.500.12657/51086/1/external_content.pdf	224,86.86,289.38,294.28,9.00;224,72.00,301.38,79.59,9.00
doc0009	cite0598	Raw_Reference	Scouts reviewed by British Minister, Panama Star and Herald, 1 Dec. 1923, enclosed in British Public Record Office, FO 371/8475, f. 105.	YES	3770ea7f24f3c2572fb7b08262bf2be9e0ca691b	http://d-scholarship.pitt.edu/20856/1/PutnamSocHist2006PostPrint.pdf
```



## Citation collection files

| File name              | # of Documents | # of Citations | # of Reference to Archive | 
| :---                   | ---:           | ---:           | ---:     |
| random-500-about.tsv   | 1,204          | 500            | 13
| random-500-strict.tsv  | 1,204          | 500            | 7
| random-1259-strict.tsv | 1,204          | 1,259          | 56
| rule-600-about.tsv     | 1,204          | 600            | 124
| svm-760-strict.tsv     | 1,204          | 760            | 47
