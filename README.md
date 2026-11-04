# Woruldende: Eschatological Vocabulary in Old English Homilies

Code and data for the paper *Woruldende: Eschatological Vocabulary in Old English Homilies* by Katrin Levy, Shai Gordin and Eliese-Sophia Lincke (Anthology of Computers and the Humanities, CHR 2027).

The project applies a TF-IDF vector space model to 19 Old English homilies by Wulfstan, Ælfric and the anonymous Blickling and Vercelli homilists, to ask whether the three author groups use distinguishable vocabulary when preaching about the end of the world.

## Contents

- `Woruldende_clean__05_Vector_Space_model.ipynb` — the analysis notebook (TF-IDF, cosine distances, t-SNE, heat map, control analyses, robustness checks).
- `corpus_csv/` — the 19 per-text CSV files used by the notebook.
- `woruldende_metadata_v3.csv` — corpus manifest (author group, approximate date, source).
- `oe_stopwords.txt` — the Old English stopword list.
- `Woruldende_robustness_grid.csv` — results of the robustness checks (Appendix A of the paper).
- `lemmatisation_notes.txt` — notes on how the `cf` column was produced and on the controls for it.

## How to run

Open the notebook in Google Colab and choose Runtime → Run all. The first cell downloads this repository, so the corpus files load automatically. No upload is needed.

## About the data

- The Wulfstan, Blickling and Vercelli texts come from the ECHOE project (https://echoe.uni-goettingen.de/), plaintext edition, licensed CC BY 4.0. ECHOE provides no lemma annotation.
- The Ælfric texts (Catholic Homilies I: I, XV, XXI, XL) come from Thorpe (1844) as transcribed on Wikisource. See Wikisource for the licence terms of the transcription.
- The `cf` column is a small hand-built dictionary (about 173 headwords) applied identically to all 19 texts; all other words remain lowercased surface forms. See `lemmatisation_notes.txt` and the paper's Limitations section.

## Acknowledgements

The notebook builds on a vector space model notebook originally developed by Avital Romach (Yale University) for Akkadian corpora, further developed by Shai Gordin and Eliese-Sophia Lincke for Egyptian. The method follows Karsdorp et al., *Humanities Data Analysis*.
