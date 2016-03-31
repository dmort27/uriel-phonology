# URIEL-Phonology

Patrick Littell, David R. Mortensen, and Lori Levin (eds.)

This release represents the source phonological feature data and calculated averages from the second release of Littel, Mortensen, and Levin (v0.1, December 2015).

## FEATURES

All files listed here have a simple tabular format, in CSV format, with ISO 639-3 language identifiers in the first column, and features at the top.  Features are [0.0, 1.0] intervals, with 1.0 representing the presence of a segment (e.g., the voiceless interdental fricative), class (voiced plosives), or phenomenon (complex syllable onsets).  0.5 represents a null value.

For example, the file might look something like:

    code, P_BILABIALS, P_CLICKS
    deu, 1.0, 0.0
    eng, 1.0, 0.0

INV_ features represent the phonetic inventory of the language, and P_ represents phonological features.  Features that share names otherwise (say, P_VOICED_PLOSIVES and INV_VOICED_PLOSIVES) should not be assumed to have identical semantics and values.  (E.g., the language might have phonetic voiced plosives but not have a )

These files are deduced from feature databases (e.g., WALS, PHOIBLE) and text databases (e.g. Ethnologue).  Each source is given as its own CSV file.

- **wals.csv** -- Features derived from the World Atlas of Language Structures.
- **ethno.csv** -- Features derived from (shallowly) parsing the prose typological descriptions in Ethnologue (Lewis et al. 2015).
- **phoible_aa.csv** -- AA = Alphabets of Africa. Features derived from PHOIBLE's normalization of *Systèmes alphabétiques des langues africaines* (Hartell 1993, Chanard 2006).
- **phoible_gm.csv** -- GM = Green and Moran.  Features derived from PHOIBLE's normalization of Christopher Green and Steven Moran's pan-African inventory database.
- **phoible-ph.csv** -- PH = PHOIBLE.  Features derived from PHOIBLE proper, by Moran, McCloy, and Wright (2012).
- **phoible-ra.csv** -- RA = Ramaswami.  Features derived from PHOIBLE's normalization of *Common Linguistic Features in Indian Languages: Phoentics* (Ramaswami 1999).
- **phoible-saphon.csv** - SAPHON = South American Phonological Inventory Database.  Features derived from PHOIBLE's normalization of SAPHON (Lev et al. 2012).
- **phoible-spa.csv** - SPA = Stanford Phonology Archive.  Features derived from PHOIBLE's normalization of SPA (Crothers et al., 1979).
- **phoible-upsid.csv** - UPSID = UCLA Phonological Segment Inventory Database.  Features derived from PHOIBLE's normalization of UPSID (Maddieson 1984, Maddieson and Precoda 1990).


## avg.csv

The above sources do not always agree on values.  The primary source used in phoible_aa might, for example, categorize a particular segment in a particular language as velar, whereas phoible_gm might categorize it as uvular.

This file contains the mean of (known) values from sources above.  That is to say, it is equal to the percentage of sources that valuate the feature at 1.0, out of sources that valuate the feature at all.  (Or, the probability of a feature being 1.0 if a source is chosen at random.)

It is in the same format as the feature charts above.
