# Third-party notices

`index.html` bundles the following third-party software. Each keeps its own license; full texts are in the `licenses/` folder.

| Component | Version | License | Source |
| --- | --- | --- | --- |
| libredwg-web (JavaScript/WebAssembly build of GNU LibreDWG) | 0.8.1 | GPL-3.0 | https://github.com/mlightcad/libredwg-web · https://www.gnu.org/software/libredwg/ |
| PDF.js (`pdfjs-dist`, legacy build) | 3.11.174 | Apache-2.0 | https://github.com/mozilla/pdf.js |

## How they are embedded

- **libredwg-web:** the WebAssembly binary is gzip-compressed and base64-encoded inside the `<script id="dwgwasm">` element; its JavaScript wrapper is bundled (minified with esbuild) in the script that follows it. The unmodified package is available from npm as `@mlightcad/libredwg-web@0.8.1`, and its complete corresponding source code is at the repository linked above.
- **PDF.js:** `legacy/build/pdf.min.js` and `legacy/build/pdf.worker.min.js` from `pdfjs-dist@3.11.174`, unmodified, are embedded as inline scripts.

The application code of this tool is the last, unminified `<script>` block in `index.html`, and is licensed under GPL-3.0 (see `LICENSE`).

Fonts are loaded at runtime from Google Fonts (IBM Plex Sans Thai, IBM Plex Mono; SIL Open Font License 1.1) and are not redistributed in this repository.
