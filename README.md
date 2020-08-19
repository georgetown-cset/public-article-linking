# Article Linking

This repository contains a description and supporting code for CSET's current method of 
cross-dataset article linking. Note that we use "article" very loosely, although in a way that to our knowledge 
is fairly consistent across corpora. Books, for example, are included.

For each article in arXiv, WOS, CNKI, Dimensions, and Microsoft Academic Graph, we normalized titles, abstracts, 
and author last names, and then considered each group of articles within or across datasets that shared at least 
three of the following (non-null) metadata fields:
 
*  Normalized title
*  Normalized abstract
*  Publication year
*  Normalized author last names
*  Citations (for within dataset matches)
*  DOI
 
to correspond to one article in the merged dataset. We add to this set "near matches" of the concatenation 
of the normalized title and abstract within a publication year, which we identify using simhash.

To do this, we run the `linkage_dag.py` on airflow. The article linkage runs weekly, triggered by the MAG dag.

For an English description of what the dag does, see [the documentation](methods_documentation/overview.md).

