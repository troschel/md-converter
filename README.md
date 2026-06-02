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
python3 md-converter.py to-docx ./source ./for_translation
```

**From .docx to .mdx/.json:** Convert the translated `.docx` files back to `.mdx`/`.json`

```bash
python3 md-converter.py from-docx ./translated ./output
```

The folder structure is preserved. Each file is named unambiguously (e.g. `page.mdx` → `page.mdx.docx` → `page.mdx`), so the mapping is always clear. The output folder is created automatically if it doesn't exist.

This script can be used to convert Markdown- or JSON-Files for translation, as professional translation services, but also LLM's tend to work better with .docx files. 
**Note when working with automatic translation**: Syntax in .json-files will also be translated and will make files unusable. If working wit LLM's or automatic translators, instruct them not to translate syntax.
