# Usage

The README covers the basics. This page collects the
longer examples and the notes that did not fit up front.

## Basic

```bash
python pipeline.py raw.csv --config config.yaml --out clean.csv
```

## Notes

- Chunked reading for files that do not fit in memory
- Writes a cleaning report next to the output
