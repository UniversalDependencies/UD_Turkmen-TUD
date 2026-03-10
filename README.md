# Summary

UD_Turkmen-TUD is a silver-standard Universal Dependencies treebank for Turkmen, created by translating Turkish UD treebank data into Turkmen and applying silver annotation through cross-lingual transfer.

# Introduction

This treebank provides dependency-annotated data for Turkmen (ISO 639-1: `tk`, ISO 639-3: `tuk`), an agglutinative Turkic language of the Southwestern (Oghuz) branch. Turkmen has approximately 11 million speakers, primarily in Turkmenistan, and uses a Latin-based orthography adopted in 1993.

The treebank was created through translation of Turkish UD data into Turkmen, followed by silver annotation.

# Data Sources

The treebank data was derived by translating sentences from the following Turkish UD treebanks into Turkmen:

**Training data** — translated from:
- [UD_Turkish-IMST](https://github.com/UniversalDependencies/UD_Turkish-IMST/blob/master/tr_imst-ud-train.conllu) (`tr_imst-ud-train.conllu`)
- [UD_Turkish-GB](https://github.com/UniversalDependencies/UD_Turkish-GB/blob/master/tr_gb-ud-test.conllu) (`tr_gb-ud-test.conllu`)
- [UD_Turkish-FrameNet](https://github.com/UniversalDependencies/UD_Turkish-FrameNet/blob/master/tr_framenet-ud-train.conllu) (`tr_framenet-ud-train.conllu`)

**Test data** — translated from:
- [ud-turkic/parallel](https://github.com/ud-turkic/parallel/blob/main/tr_tuecl-ud-test.fa.conllu) (`tr_tuecl-ud-test.fa.conllu`)

# Methodology

1. Source sentences from the Turkish UD treebanks listed above were translated into Turkmen.
2. Annotations (POS tags, morphological features, dependency relations) were projected through silver annotation via cross-lingual transfer.
3. Language-specific annotation guidelines for Turkmen were developed following UD v2 conventions (see `turkmen_ud.md`).

# Data Splits

| Split | Sentences | Tokens |
|-------|-----------|--------|
| Train | 6,344     | 41,992 |
| Dev   | 704       | 4,667  |
| Test  | 141       | 839    |

The dev split was randomly sampled (10%, seed=42) from the original training data.

# Genres

The treebank covers multiple genres inherited from the source Turkish treebanks, including news, non-fiction, and web text.

# Annotation

Annotations are silver-standard, produced through cross-lingual transfer from Turkish UD annotations. The treebank uses all 17 Universal POS tags and annotates morphological features including Case, Number, Person, Tense, Aspect, Mood, Evidentiality, Voice, and Polarity, following Turkmen-specific conventions documented in the language guidelines.

# Acknowledgments

This treebank was developed as part of the [TurkicNLP toolkit](https://turkic-nlp.github.io/) initiative to harmonize and expand Universal Dependencies coverage for Turkic languages.

We gratefully acknowledge the creators of the source Turkish treebanks:
- UD_Turkish-IMST (Sulubacak et al.)
- UD_Turkish-GB (Guilherme et al.)
- UD_Turkish-FrameNet (Çöltekin et al.)

# References

```
@misc{hakimov2026turkicnlpnlptoolkit,
      title={TurkicNLP: An NLP Toolkit for Turkic Languages}, 
      author={Sherzod Hakimov},
      year={2026},
      eprint={2602.19174},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2602.19174}, 
}
```

# Changelog

* 2026-03-09 v0.1
  * Initial silver-annotated treebank created from Turkish-to-Turkmen translation.

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD vX.X
License: CC BY-SA 4.0
Includes text: yes
Genre: news nonfiction web
Lemmas: automatic
UPOS: automatic
XPOS: not available
Features: automatic
Relations: automatic
Contributors: Hakimov, Sherzod
Contributing: github
Contact: sherzodhakimov@gmail.com
===============================================================================
</pre>
