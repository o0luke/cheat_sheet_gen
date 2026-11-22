# Cheat Sheet Generator

A browser-based cheat sheet generator that turns plain text into a printable, multi-page A4 layout. Adjust the typography and spacing in a live preview, then export the result as a PDF.
Live: https://cheatsheetgen.netlify.app/

## Features

- Live preview while entering or editing text
- A4 portrait sheets with eight printable sections per sheet
- Automatic text fitting and pagination
- Controls for:
  - Font family
  - Font size
  - Line height
  - Text padding
  - Text alignment
- Page numbering that follows the generated reading order
- PDF export using `html2pdf.js`
- Responsive layout for desktop and smaller screens
- No build step or server-side code required

## Getting started

### Run locally

The project is a standalone HTML file. Open [`index.html`](./index.html) directly in a modern browser, or serve the folder with any local static web server:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

### Use the generator

1. Paste or type your notes into **Text Content**.
2. Choose the font family and font size.
3. Adjust line height, padding, and alignment as needed.
4. Review the generated pages in the preview area.
5. Select **Download PDF** and confirm the usage disclaimer.

The generated PDF is saved as `cheatsheet.pdf`.

## How it works

The application divides each A4 page into a two-column by four-row grid. Text is distributed across paired sheets in the order required for the printed and folded cheat-sheet layout. Each section is measured in the browser, and a binary-search fitting routine keeps text inside its available area before continuing on the next section.

## Dependencies

The app loads these external resources from CDNs:

- [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) from Google Fonts
- [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) from cdnjs

An internet connection is required when these resources are not already cached by the browser.

## Project structure

```text
.
├── index.html   # Application markup, styles, and JavaScript
└── README.md    # Project documentation
```

## Responsible use

Use this tool responsibly and only for ethical and lawful purposes. The application is intended for organizing legitimate study notes and reference material.

## License

No license has been specified for this project yet.
