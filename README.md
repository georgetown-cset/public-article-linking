# Article Linking
![Python application](https://github.com/georgetown-cset/article-linking/workflows/Python%20application/badge.svg)

This repository contains a description and supporting code for CSET's initial (as of February) method of 
article linking. We have since made improvements, such as including simhash matches of title+abstracts,
modifications to make updates to the linkage more efficient, and executing the linkage with Airflow, which
we will publish in a later commit to this public repo. The documentation comes in four parts starting with
 [metadata normalization](methods_documentation/0_metadata_table_generation.md). This section describes
how we put a subset of metadata across arXiv, Web of Science, Dimensions, and Microsoft Academic
Graph into a common format, and then normalized that data.

Note that throughout, we use "article" very loosely, although in a way that to our knowledge is fairly
consistent across corpora. Books, for example, are included. For full details, see the queries in section 1.
