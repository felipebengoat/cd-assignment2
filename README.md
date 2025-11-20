## Annotations and Tools
- **Tool**: spaCy (`en_core_web_sm`)
- **Tokens**: Word tokens as segmented by spaCy’s tokenizer
- **Lemmas**: Base forms of tokens (e.g., "running" → "run")
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

## Notes
This assignment follows the workflow demonstrated in the official lab notebook:  
[https://github.com/yevgenm/corpus-analysis-spacy](https://github.com/yevgenm/corpus-analysis-spacy)