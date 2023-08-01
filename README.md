# Archive Citation Collection

This test collection consists a total 3,999 of annotated passages whether it referes to a reference to an archive from open access scholarly literature of over 1,3000 documents crawled using [the Semantic Scholar API](https://www.semanticscholar.org/product/api). This test collection was constructed for evaluating a system's performance to classify whether a given passage is a reference to an archive or not.

## Data

This test collection includes four TSV (Tab-separated values) files shown the below. 

1. ``` subset-1_random-500-strict-about.tsv```
1. ``` subset-2_Rule-600-strict-about.tsv```
1. ``` subset-3_svm-760-strict.tsv```
1. ``` subset-4_random-rule-1260-strict.tsv```

Each table file contains about 500 - 1200 labeled citations. These table files consist of the following columns:

- ``` Doc_ID ```: an identifier for an documents in this test collection.
- ``` Cite_ID ```: an identifier for a citations in this test collection.
- ``` Contents ```: a citation OCR text extracted by the PDF parsing software [GROBID](https://github.com/kermitt2/grobid). 
- ``` Label ```: an annotated label. When ```STRICT```, the citation is one or several references to archives. When ```ABOUT```, the citation includes an explanatory text in addition to one or several references to archives. A blank indicates that the citation is not in the above two labels. 
- ``` Paper_ID ```: an identifier of a paper provided by [the Semantic Scholar Academic Graph (S2AG)](https://www.semanticscholar.org/product/api) API.
- ``` URL ```: the source URL of the document.
- ``` Docment_part ```: a document part of a PDF document where a citation is detected. This field has two values, "Raw_reference" and "FootNote". "Raw_reference" stands for that a citation is found in the end of document such as reference section or endnote section. "FootNote" stands for that a citation is found in a footnote.
- ``` Coords ```: a coordinate where a citation is located on a PDF file detected by GROBID. This coordinate information are available on some of the citations which GROBID successfully detected.


## Citation collection files

| File name                              | # of Documents | # of Citations  | # of Strict citations |  # of About citations
| :---                                   | ---:           | ---:    | ---:  | ---:     |
| subset-1_random-500-strict-about.tsv   | 1,204          | 498     | 7     | 4  
| subset-2_Rule-600-strict-about.tsv.    | 1,204          | 574     | 107   | 17 
| subset-3_svm-760-strict.tsv            | 1,204          | 760     | 47    | -
| subset-4_random-rule-1260-strict.tsv   | 1,204          | 1,256   | 56    | -