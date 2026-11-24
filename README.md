# Niklas Köhne

**I build NLP and retrieval systems for messy, historical text, and I measure whether they work.**

Trained lawyer (LL.B.) and PhD researcher at the University of Münster. My data is about 4,000 medieval Latin letters (1.6M tokens) with
inconsistent spelling, no training labels, and licensing rules on what may be sent where.
I've turned that into a tested pipeline that goes from scanned edition to source-cited answers.

## Projects

**nlp-suite** · Python · NLP toolkit for low-resource historical corpora · *public release in preparation*
- Spelling normalisation with a lexicon as checker; every change logged and reversible
- Standoff annotation layers (lemmas, named entities, dates, citations) over an unchanged source text
- Evaluation harness: scores any layer against gold data, with bootstrap confidence intervals
- Reproducible runs: each run writes a manifest (models, versions, parameters, input hashes, git commit)
- Data-governance policy in code: refuses to send a licensed corpus to a model that may not see it
- Benchmarked three NLP stacks (LatinCy/spaCy, Stanza, CLTK) on lemmatisation and POS tagging

**Retrieval-augmented QA over a 4,000-letter corpus** · Python · *private: the edition text is under copyright*
PDF → structured records → normalised tokens → hybrid retrieval (BGE-M3 dense embeddings + BM25, LanceDB and SQLite FTS5)
→ cross-encoder reranking → answers with verified source citations. Retrieval quality measured with nDCG on a hand-built test set.

## Stack

**Python** (uv, pytest, spaCy, Stanza, Hugging Face) · **retrieval** (dense + sparse hybrid, reranking, LanceDB, SQLite FTS5) ·
**evaluation** (nDCG, precision/recall, bootstrap CIs, gold-set design) · **LLM engineering** (RAG, local and hosted models, agentic coding workflows) ·
Docker, self-hosted services · Git

## How I work

I build with AI coding agents and say so: commits carry a `Co-Authored-By` line.
I own the problem framing, architecture, data rules and tests; agents write much of the code under them,
and every result is checked against the data.

## More

[CV](cv.md) · full CV on request via the email on my GitHub profile
