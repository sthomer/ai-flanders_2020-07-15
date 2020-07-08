# AI Flanders Presentation (July 15, 2020)

The layout of the document is as follows:
- `presentation.tex` contains the packages, theming, title slide, and final slide
- `nick/presentation.tex` contains Nick's portion of the presentation
- `steve/presentation.tex` contains Steve's portion of the presentation
- `template.tex` contains a few template slides to make the presentation more cohesive
- `images` will contain all the graphics assets, i.e. `\includegraphics{images/asset.png}`

It is suggested to use the latexmk build tool for producing the pdf:
`latexmk -pvc -pdflatex presentation.tex`
Keep this running in a terminal to automatically update the pdf whenever the document is saved.

---

# Outline suggested during the conversation on July 6, 2020

## Nick
Nick should demonstrate progress on the discrete resonance spectrogram primarily through three avenues:
- Progress on FPT filters
  - Compare DSR visually with FFT and unfiltered DSR
- F0 estimation / Pitch-to-Midi
  - Moving from the "continuous" spectrum to the "symbolic" notes
- Source/voice separation
  - Discrete spectral signature of a given source (regardless of audio context?)

## Steve
Steve should link work to sequential speech model and demonstrate progress using segmentation and network theory: 
- Current DSR operates one slice at a time, but temporal correlations in the sequence can be exploited
  - Hierarchical Markov chains capture short- and long-term dependencies
- Complex network theory provides natural way to examine Markovian structure and dynamics
  - Community structure of networks
  - Minimum Description Length principle for networks
- Boundary entropy segmentation of a sequence or network
  - Sequence interpretation of boundary entropy segmentation
  - Network interpretation of boundary entropy segmentation
