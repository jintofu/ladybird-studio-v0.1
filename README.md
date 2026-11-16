# LadyBird Studio — DNA Sonification Lab

A static, browser-based prototype for exploring DNA-to-music mapping. It runs entirely in the browser and does not upload sequence data.

## Features in v0.1

- Paste DNA sequence or upload FASTA/TXT.
- Validate A/T/C/G and ambiguous N symbols.
- Forward and reverse-complement strand selection.
- Reading frames +1, +2, +3.
- Standard genetic-code translation.
- Three sonification modes: nucleotide, codon identity, and amino-acid mapping.
- Musical presets: chromatic, major, minor, pentatonic, and editable custom pitch map for nucleotide and codon modes.
- Browser audio playback using Web Audio API.
- Export WAV, MIDI, PNG visual score, and experiment JSON.
- Local-only processing; no API key or backend.

## Run locally

Open `index.html` in a modern browser (Chrome, Edge, Firefox, or Safari). Audio playback requires a user click and a browser with Web Audio support.

Alternatively, run a local static server:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Publish with GitHub Pages

1. Create a new GitHub repository, for example `ladybird-studio`.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. The site URL will be shown in the Pages settings, typically `https://YOUR-USERNAME.github.io/ladybird-studio/`.

No build step is required.

## Important scientific notes

This is an artistic sonification tool, not a clinical or bioinformatics annotation system. It translates the selected input according to the chosen reading frame and the standard genetic code. It does not identify CDS regions, exons, introns, UTRs, canonical transcripts, or the correct LBX1 reference sequence automatically. For a meaningful protein translation, supply a verified coding sequence (CDS) and record organism, accession/version, transcript, strand, frame, and genetic code table.

Pitch assignments are compositional conventions. They are not intrinsic biological frequencies or scientifically validated representations of amino-acid properties.

## Suggested next development steps

- Implement truly editable custom mapping for each nucleotide, codon, and amino acid.
- Add NCBI/Ensembl retrieval with accession/version provenance.
- Add annotated gene structures (CDS/exon/intron/UTR) from a trusted annotation source.
- Add multi-track composition, harmony layers, and DAW-style editing.
- Add automated unit tests for translation and MIDI/WAV export.
