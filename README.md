# arabic-doc-parser

Turn Arabic and mixed Arabic/English PDFs and scanned pages into clean, RAG-ready Markdown.

> Status: early development. APIs will change.

## Why

Most document parsers break on Arabic: reversed text, broken letters, lost tables, and mixed RTL/LTR lines. `arabic-doc-parser` focuses on getting Arabic documents right, so they can be searched, chunked, and used in RAG pipelines.

## Planned features

- [ ] Text extraction from digital PDFs with correct RTL ordering
- [ ] OCR for scanned pages and phone photos (Arabic + English)
- [ ] Headings, lists, and paragraphs to Markdown
- [ ] Table extraction for mixed Arabic/English tables
- [ ] Arabic text normalization (diacritics, hamza forms, Arabic-Indic digits, broken words)
- [ ] RAG-ready chunking with page-number metadata
- [ ] Equations and code blocks preserved as LaTeX / fenced code
- [ ] Quality and speed benchmarks on sample documents
- [ ] CLI and Python API
- [ ] Published on PyPI

## Planned usage

```bash
pip install arabic-doc-parser
arabic-doc-parser convert notes.pdf -o notes.md
arabic-doc-parser chunk notes.pdf --size 800 -o chunks.jsonl
```

```python
from arabic_doc_parser import convert

markdown = convert("notes.pdf")
```

## Roadmap

1. Project setup: packaging, CLI, tests, CI
2. Digital PDF extraction with RTL handling
3. OCR for scanned pages
4. Layout to Markdown (headings, lists, paragraphs)
5. Tables
6. Arabic normalization
7. Chunking for RAG
8. Equations and code
9. Benchmarks
10. Docs, examples, PyPI release

## Contributing

Issues and pull requests are welcome. Please do not upload documents that contain other people's personal data in issues or tests.

## License

MIT, see [LICENSE](LICENSE).
