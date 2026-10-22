# 🧬 DNA Sequence Analyzer

**A lightweight, browser-based bioinformatics dashboard for exploring DNA sequences from FASTA files or pasted nucleotide text.**

DNA Sequence Analyzer turns raw DNA sequence input into an interactive summary with nucleotide composition, GC/AT content, regional GC distribution, reverse complement, and an RNA-style sequence view. It is designed as an educational portfolio project for students learning bioinformatics and sequence analysis.

## ✨ Features

- **FASTA input:** Paste sequence text or upload `.fasta`, `.fa`, `.fna`, or `.txt` files.
- **Multi-FASTA support:** Load multiple records and choose which record to inspect.
- **Sequence statistics:** Calculate sequence length and A/T/G/C counts and percentages.
- **GC and AT content:** Summarize overall nucleotide composition.
- **Visualizations:** View a nucleotide composition doughnut chart and a sliding-window regional GC% plot.
- **Sequence workbench:** Explore the reverse complement, a color-coded sequence view, and a T-to-U sequence conversion.
- **Export tools:** Download a reverse-complement FASTA file or export summary metrics as CSV.
- **Responsive interface:** Dashboard layout designed for desktop and mobile screens.

## 🚀 Run locally

No build step is required.

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Paste a DNA sequence in FASTA format, upload a FASTA file, or click **Load Sample FASTA**.
4. Click **Analyze DNA Sequence**.
5. Explore the dashboard and use the export buttons if needed.

### Optional: serve it locally

From the repository directory, run:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000> in your browser.

## 🧪 Example input

```fasta
>DNA_001 Example sequence
ATGCATGCATGC
```

For this 12-base example, the expected overall values are:

- Length: `12 bp`
- A: `3`, T: `3`, G: `3`, C: `3`
- GC content: `50.00%`
- AT content: `50.00%`
- Reverse complement: `GCATGCATGCAT`

## 🧰 Technologies

- HTML5
- CSS with Tailwind CSS (loaded from CDN)
- Vanilla JavaScript
- Chart.js (loaded from CDN)
- Font Awesome icons and Google Fonts (loaded from CDN)

An internet connection is required for the externally hosted styling, charting, icon, and font assets to load as intended. The sequence calculations themselves run in the browser.

## 📁 Repository structure

```text
dna-sequence-analyzer/
├── index.html
├── README.md
└── LICENSE
```

## ⚠️ Notes and limitations

- This is an educational sequence-analysis tool, not a clinical or diagnostic application.
- Results depend on the sequence provided and the assumptions used by the calculations.
- Melting-temperature and molecular-mass values are approximate estimates; they should not be treated as experimentally validated measurements.
- The interface recognizes common IUPAC ambiguity symbols for reverse-complement mapping, but users should verify input compatibility before interpreting quantitative results.
- Uploaded sequence data is processed by the browser-side JavaScript in this page; avoid entering sensitive or restricted data into any online tool unless its privacy properties have been independently reviewed.

## 🛣️ Possible future improvements

- Add automated tests for sequence parsing and calculation functions.
- Add clearer validation for unsupported nucleotide characters.
- Provide downloadable analysis reports with method notes.
- Improve handling and documentation of ambiguity codes in GC/AT calculations.
- Add an offline-friendly version with local copies of third-party assets.

## 📄 Author

Tushar Sain
Bioinformatics | Genomics | Computational Biology

Made for learning and exploring computational biology, one sequence at a time. 🧬
