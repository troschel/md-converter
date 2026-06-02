# MDX/JSON-Converter

A small Python utility to convert `.mdx` and `.json` files to `.docx` for translation services that only accept Word documents — and back again.

## Requirements

- Python 3
- [python-docx](https://python-docx.readthedocs.io/)

```bash
pip install python-docx
```

## Usage

**From .mdx/.json to .docx:** Convert your source files to `.docx`

```bash
python3 convert_for_translation.py to-docx ./source ./for_translation
```

**From .docx to .mdx/.json:** Convert the translated `.docx` files back to `.mdx`/`.json`

```bash
python3 convert_for_translation.py from-docx ./translated ./output
```

The folder structure is preserved. Each file is named unambiguously (e.g. `page.mdx` → `page.mdx.docx` → `page.mdx`), so the mapping is always clear. The output folder is created automatically if it doesn't exist.
