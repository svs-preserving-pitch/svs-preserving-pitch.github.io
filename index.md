# <center> Pitch Preservation In Singing Voice Synthesis </center>
<center> Shujun liu<sup>1</sup>, Author2<sup>2</sup> </center>

## Abstract
Suffering from limited singing voice corpus, 
existing advanced singing voice synthesis (SVS) methods that build encoder-decoder neural network to generate mel-spectrogram could lead to out-of-tune issues during inference phase.
To attenuate this issues,
this paper presents novel methods of pitch metric learning and pitch domain adaptation for acoustic encoder by leveraging the intrinsic linear relationship between pitches and pitch prior respectively.
Because all pithes in an octave are arranged in a geometric sequence according to equal temperament theory,
we design a pitch encoder followed by a metric loss that maps distances between adjacent pitch inputs into corresponding frequency multiples between the encoder outputs.
Besides,
based on the analysis that a phoneme corresponding to varying pitches can produce similar pronunciations,
we design another phoneme encoder with an adversarially trained pitch classifier  to enforce identical phonemes with different pitches mapping into the same phoneme feature space.
The classifier integrates pitch prior, disentangling the phoneme and pitch information further.
Then, the outputs of  the pitch encoder and phoneme are summed together to pass through following decoder.
Experiments indicate that the proposed SVS approach is capable of enhancing the performance of synthesizing sparse couples of phoneme and pitch,
and can characterize the intrinsic structure of pitches to obtain better pitch synthesis accuracy against baseline.

---
## Some synthesized samples

|Recording| Baseline | Baseline + pm | Baseline + pc | Baseline + pm + pc |
|      -  |     -    |     -         |        -      |           -        |
| <audio src="white.wav"></audio> |          |               |               |                    |
