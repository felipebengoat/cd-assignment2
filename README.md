# Personal Letters Corpus: Luis Mitrovic Archive
## Corpus Description

This corpus consists of 15 English-language personal letters from the private archive of Chilean architect and photographer **Luis Mitrovic Balbontín** (1911–2008) that is being preserved and digitilized by Fundación Enterreno (Chile) since 2023. The letters include both correspondence written by Mitrovic and letters he received, spanning various topics including professional architecture discussions, personal updates, and cultural observations. These documents were originally handwritten or typed and later digitized for preservation and linguistic analysis. This is a sample of 15 letters, but the entirity of the archive reaches more than 3.000 letters.

### Digitization and Preparation Process
- The original physical documents were digitized using proffessional equipments and softwares by Fundación Enterreno (Chile).
- OCR was performed using **Qwen3-Max**, which enabled accurate transcription of typed and handwritten passages.
- Transcribed texts were initially organized in an Excel spreadsheet to associate each document with its metadata (e.g., filename, date, recipient).
- Full letter contents were then extracted and saved as individual plain-text files (`.txt`) in the `data/` directory to form the final corpus.
- 
## Target Audience and Intended Use
This corpus is intended for:
- **Linguistic researchers** studying historical epistolary English and personal correspondence patterns
- **Digital humanities scholars** interested in archival digitization and personal document analysis
- **NLP practitioners** seeking authentic historical text data for training or testing language models
- **Students** learning corpus creation, text preprocessing, and linguistic annotation workflows

## Annotations and Tools
- **Tool**: spaCy (`en_core_web_sm`)
- **Tokens**: Word tokens as segmented by spaCy’s tokenizer
- **Lemmas**: Base forms of tokens (e.g., "running" to "run")
- **Parts-of-speech**: Universal POS tags (e.g., NOUN, VERB, ADJ, ADV)
- **Named Entities**: Extracted using spaCy’s NER component and stored in the format `text/LABEL` (e.g., `"United Nations/ORG"`)

## File Formats
- `data/*.txt`: Raw text files (UTF-8 encoding)
- `corpus.csv`: Fully annotated corpus with one row per document
- `corpus_processing.ipynb`: Jupyter Notebook containing all code for preprocessing and annotation

## CSV Column Description
| Column | Description |
|--------|-------------|
| `Filename` | Name of the source `.txt` file |
| `Title` | Not provided (`NULL`) |
| `Document` | Original text exactly as read from file |
| `Text` | Not used (`NULL`) |
| `Tokens` | Space-separated word tokens |
| `Lemmas` | Space-separated lemmatized forms |
| `Parts-of-speech` | Space-separated universal POS tags |
| `Named_Entities` | Named entities in `text/LABEL` format, separated by ` \| ` |

## Quality Checks
- All 15 text files are readable and non-empty.
- Total token count: **12,948** (slightly above the recommended 10,000-token limit, but retained to maintain genre diversity).
- Total folder size: **< 1 MB** (well under the 100 MB hard limit).
- The Jupyter Notebook runs end-to-end and reproduces the `corpus.csv` file exactly.

### Code Adaptation and Assistance
The Jupyter Notebook code for preprocessing and linguistic annotation was developed with the assistance of **Qwen3-Max**, which helped adapt the workflow from the [spaCy corpus analysis lab](https://github.com/yevgenm/corpus-analysis-spacy) to this specific dataset. All processing steps, including tokenization, lemmatization, part-of-speech tagging, and named entity recognition, were executed using spaCy’s `en_core_web_sm` pipeline, as described in this README.

## Citation

If you use this corpus in your research, please cite or contact: Felipe Bengoa and Fundación Enterreno.
