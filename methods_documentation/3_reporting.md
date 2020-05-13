## Results

Our current method is extremely simple. Nevertheless, we were able to match the following
percentages of the datasets to each other (self-matches included):

arXiv-WOS | 49.33%

arXiv-DS | 99.68%

arXiv-MAG | 93.32%

WOS-DS | 66.40%

WOS-MAG | 70.52%

DS-MAG | 75.96%

Resulting in 213,965,351 total articles. The match rates for the subset of articles that had abstracts were
significantly better.

We have two tables to help you use these results:

- `gcp_cset_links_v2.article_links` - Gives for each original ID (e.g., from WoS) the corresponding CSET ID. 
This is a many-to-one mapping. Each original id (`orig_id`) is mapped to exactly one CSET id (`merged_id`), 
but there can be many original ids linked to a CSET id.

- `gcp_cset_links_v2.article_merged_metadata` - This maps the "CSET" `merged_id` to merged metadata