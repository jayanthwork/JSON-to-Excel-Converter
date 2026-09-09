# JSON → Excel Converter

Deployment-ready, fully offline website.

This version creates a real `.xlsx` Excel workbook (OOXML), not XML content renamed to `.xlsx`.

Rules:
- If JSON contains `Data` as an array, only `Data[]` is exported.
- `Data` is not an Excel column.
- Top-level `Status` is ignored.
- `ownerVatNumber` and `materialCode` are excluded by default.
- Other fields inside `Data[]` become columns.
- Each `Data[]` object becomes one row.
- Nested objects are flattened with dotted column names.

Keep `index.html` and `jszip.min.js` in the same folder. No internet or backend is required.
