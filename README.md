# Simple-Drum-Music-GAN
This GAN, based off the MNIST GAN tutorial from Tensorflow, generates MIDI files of drum tracks of tunable length, using 3 discriminators whose weighted average decisions are sent to the generator for calculating loss.
Results are of mixed quality...The best MIDIs are generated in epochs 0-20, with only 0-3 being usable (0 most common). But when the tracks are usable, they are in 4/4 and contain well-defined measures built off of the counts 1 & 3 = bass, 2 & 4 = snare common paradigm for rock/metal/funk drumming. 

The use of 3 discriminators is based off of tuning one for general dimension reduction of 2D input data, another for one-sided dimension reduction (the less important dimension is reduced quickly first, then the remaining reductions are slow), and the last for the other component's one-sided dimension reduction.

The data used comes from Magenta's tensorflow datasets, and is the extended midi drum files dataset, E-GMD. Available at https://magenta.tensorflow.org/datasets/e-gmd

Proper citation:
Lee Callender, Curtis Hawthorne, and Jesse Engel. "Improving Perceptual Quality
  of Drum Transcription with the Expanded Groove MIDI Dataset." 2020.
  arXiv:2004.00188.
