# Uses-friendly extensions to MeSH

The [Medical Subject Headings](https://www.nlm.nih.gov/mesh/) (MeSH) is a controled vocabulary produced by the NLM for cataloging biomedical information. The resource is structured as an ontology and is used for PubMed/MEDLINE annotation. Here we provide user-friendly datasets derived from MeSH. Currently, two [record types](https://www.nlm.nih.gov/mesh/intro_record_types.html "MeSH Record Types") are processed: Descriptors and Supplementary Concept Records.


## Notebooks

+ [`descriptors.ipynb`](descriptors.ipynb) — processes Descriptors (also known as Main Headings)
+ [`supplementary-concept-records.ipynb`](supplementary-concept-records.ipynb) — processes Supplementary Concept Records (SCRs)

## Datasets

The `data` directory contains the created datasets:

+ [`terms.tsv`](data/terms.tsv) — table of Descriptor terms.
+ [`descriptor-terms.tsv`](data/descriptor-terms.tsv) — table of Descriptor names.
+ [`mesh.json`](data/mesh.json) — a JSON-formatted representation of the Descriptor ontology. Includes term identifiers, names, semantic types, parents, and tree numbers.
+ [`ontology.gexf.gz`](data/ontology.gexf.gz) — a [GEXF](https://gephi.org/gexf/format/) representation of the descriptor ontology that is compatable with [`newtorkx`](https://networkx.github.io/).
+ [`symptoms.tsv`](data/symptoms.tsv) — symptom Descriptors (the 438 descendants of [`D012816`](http://www.ncbi.nlm.nih.gov/mesh/D012816 "MeSH Descriptor: Signs and Symptoms")
+ [`tree-numbers.tsv`](data/tree-numbers.tsv) — table of tree numbers for each Descriptor. A tree number represents a path to the the root. This file is handy for mapping to external resources which occasionally identify MeSH Descriptors by their tree numbers (a bad but prevalent practice).
+ [`supplemental-records.tsv`](data/supplemental-records.tsv) — table of SCR terms.
+ [`supplemental-terms.tsv`](data/supplemental-terms.tsv) — table of SCR names.

## License

This repository is released as [CC0](https://creativecommons.org/publicdomain/zero/1.0/ "Creative Commoms · CC0 1.0 Universal · Public Domain Dedication")
