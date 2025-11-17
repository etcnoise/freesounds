# freesounds
Some Creative Commons samples from [freesound.org](https://freesound.org) that can be used with music making environments such as [Strudel](https://strudel.cc) or [Tidal Cycles](https://tidalcycles.org).

## Licensing
Refer to the `LICENSE.md` contained in each sound folder for license information. See [Creative Commons](https://creativecommons.org/share-your-work/cclicenses/) for license details.

# PitchSample
A Haskell module that exports a single function, `pitchSample`. This function takes two arguments:
  1. `samp`: A String Pattern of samples with the folder name convention of `samplename_<key>` where `key` is a 1-3 character string that represents the key signature of the sample. `key` takes the form `R[A][M]` where:
      1. `R` is the root note (`c, d, e, f, g, a, b`)
      2. `A` is the optional accidental (`b, s` for flat and sharp respectively)
      3. `M` is the optional mode (`m` for minor, empty for major)
  2. `targetKey` A String Pattern of key signature(s)

and outputs a control pattern that pitches the samples according to the target key signatures.

Usage example:
`d1 $ pitchSample "pianoimp_eb pianoim_fm" "c"`